# Sync Iterator helpers

## TL;DR

イテレータにArrayと同じヘルパー関数が実装された（一部）。

```typescript
const iter = [1,2,3][Symbol.iterator]();

for (valur of iter) {
    ...
}

// フィルタ
iter.filter(() => {});

// 2回だけ
iter.take(1);

// オフセット
iter.drop(2);

// フラット
iter.flatMap(() => {});

// reduce
iter.reduce(() => {});

// Arrayに変換
iter.toArray();
```

find、includesなど間を飛ばすメソッドには非対応。\
sort、reverseなど順番を変更するメソッドには非対応。
