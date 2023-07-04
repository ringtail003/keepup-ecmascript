# 配列の非破壊操作

配列そのものを更新するメソッドについて `to{動詞}ed` という新たなメソッドが追加された。

例：sort（従来）toSorted（追加）

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
