# array grouping

`Object.groupBy` と `Map.groupBy` が追加された。

```javascript
Object.groupBy([1,2,3,4,5], v => v %2 === 0 ? "even" : "odd");

> {
  even: 1,3,5,
  odd: 2,4,
}
```
