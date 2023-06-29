# toSorted, toReversed

非破壊の配列操作。

## sort()

従来の関数では変数そのものが変更される。

```typescript
const array1 = [3, 4, 1, 2];
array1.sort();

console.log(array1);
> [ 1, 2, 3, 4 ]
```

## toSorted()

変数を変更せず、変更した値を返す。

```typescript
const array2 = [3, 4, 1, 2];

console.log(array2.toSorted());
> [1,2,3,4]

console.log(array2);
> [3,4,1,2]
```

## toReversed()

変数を変更せず、逆順の値を返す。

```typescript
const array3 = ["a", "b", "c"];

console.log(array3.toReversed());
> ["c", "b", "a"]

console.log(array3);
> ["a", "b", "c"]
```
