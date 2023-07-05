---
description: 非破壊操作
---

# 配列の非破壊操作

配列そのものを更新するメソッドについて `to{動詞}ed` という新たなメソッドが追加された。

## toSorted()

並べ替え

```typescript
const array = [3,4,1,2];

array.toSorted();
> [1,2,3,4]

array;
> [3,4,1,2]
```

従来の操作： `sort`&#x20;

## toReversed()

逆順に並べ替え

```typescript
const array = ["a","b","c"];

array.toReversed();
> ["c","b","a"]

array;
> ["a","b","c"]
```

従来の操作： `reverse`

## toSpliced()

つぎ足し、挙動を利用して削除に使われる事が多い

```typescript
const array = [1,2,3];

array.toSpliced(1,1,"a");
> [1,"a",3]

array;
> [1,2,3]
```

従来の操作： `splice`

## with

従来では `splice` を使う事が多かった。\
spliceの意味合いは「継ぎ足し」で、特定の部分を削除し別のものを埋め込む挙動をする。\
削除・置換どちらも利用シーンが多く、引数指定の数を覚えないといけないのでミスしやすい。

```typescript
// 削除するケース
const array = [1,2,3];
array.splice(1,1);
array;
> [1,3]

// 置換するケース（要素を削除して別のものを埋め込む）
const array = [1,2,3];
array.splice(1,1,"a");
array;
> [1,"a",3]
```

追加された `with` は置換専用のため引数の数は常に2つ。\
配列そのものは変更せず、変更後の値をリターンする。

```typescript
const array = [1,2,3];

array.with(1,"a");
> [1,"a",3]

array;
> [1,2,3]
```
