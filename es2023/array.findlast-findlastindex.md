# Array.findLast, findLastIndex

## findLast

```typescript
const array = [1,10,100];

array.findLast(v => v >= 10);
> 100
```

## findLastIndex

```typescript
const array = [1,10,100];

array.findLastIndex(v => v >= 10);
> 2
```

## 既存のメソッド

最初に見つかった要素が欲しい時は `find` `findIndex` を使う。

```typescript
const array = [1,10,100];

array.find(v => v >= 10);
> 10

array.findIndex(v => v >= 10);
> 1
```
