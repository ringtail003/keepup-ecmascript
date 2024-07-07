# Promise withResolvers

Promise, resolve, rejectを生成するユーティリティ。

```javascript
// 従来このようなユーティリティがよく使われていた。
function withResolvers() {
  let resolve;
  let reject;
  const promise = new Promise((res, rej) => {
    resolve = res;
    reject = rej;
  });
  
  return { promise, resolve, reject };
}
```

コールバックスタイルの関数の非同期処理化ができる。

```javascript
function readFileSync(path) {
  const reader = new FileReader(path);
  const { promise, resolve, reject } = withResolvers();
  reader.onerror = reject;
  reader.onload = resolve;
  reader.readAsText();
  
  return promise;
}

await textOrError = readFileSync().catch(() => "失敗");
```

ユーティリティを宣言せずともPromiseオブジェクトから呼び出せるようになった。

```javascript
const { promise, resolve, reject } = Promise.withResolvers();
```

参考：使いどころが分かりやすい。\
[https://blog.jxck.io/entries/2024-02-10/promise.withresolvers.html](https://blog.jxck.io/entries/2024-02-10/promise.withresolvers.html)
