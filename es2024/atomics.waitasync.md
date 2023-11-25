# Atomics.waitAsync

Atomics.waitの非同期メソッドが追加された。

```typescript
Atomics.waitAsync();
```

JSでメモリを共有するにはSharedArrayBufferを使う。\
SharedArrayBufferに対する操作としてAtomicsを使う。

[https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global\_Objects/Atomics](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global\_Objects/Atomics)

```typescript
const sab = new SharedArrayBuffer(100);
const uint = new Uint8Array(sab);

Atomics.add(uint, 0, 100); // index:0に100足す
```

Atomics.waitの戻り値にtimeoutがあることから、タイムアウトすることがあるらしい。
