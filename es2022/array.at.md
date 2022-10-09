# Array.at

{% embed url="https://github.com/tc39/proposal-relative-indexing-method" %}

インデックス指定で値を取り出す `Array.at` `String.at` が使えるようになった。

### Example

```javascript
const array = [1, 2, 3];
array.at(0); // 1
array.at(1); // 2
array.at(2); // 3

const string = "123";
string.at(0); // "1"
```

マイナスを指定すると末尾からの取り出しになる。

```javascript
const array = [1, 2, 3];
array.at(-1); // 3
```

### Link

{% embed url="https://caniuse.com/mdn-javascript_builtins_array_at" %}

{% embed url="https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/at" %}
