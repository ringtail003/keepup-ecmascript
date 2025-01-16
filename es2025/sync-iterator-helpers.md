# Sync Iterator helpers

{% embed url="https://github.com/tc39/proposal-iterator-helpers" %}

## TL;DR

イテレータにArrayと同じヘルパー関数が実装され、配列のように操作できるようになった。\
findやincludesなど間をとばすメソッド、sortなど順番変更するメソッドは実装されていない。

```typescript
const iter = [1,2,3][Symbol.iterator]();

for (valur of iter) {
    ...
}

iter.filter(() => {});
iter.flatMap(() => {});
iter.reduce(() => {});
iter.toArray();

// 2回だけ
iter.take(1);

// オフセット指定で削除
iter.drop(2);
```
