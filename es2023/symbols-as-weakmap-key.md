# Symbols as WeakMap key

WeakMapのキーにシンボルが使えるようになった。

```typescript
const map = new WeakMap();
const key = Symbol("ref");

map.set(key, 1);
map.get(key);
> 1
```

Symbolなのでキーの実体を知らない箇所では中身の値を取り出せない。

```typescript
weak.set(new Symbol("ref"),2); // error
weak.get(new Symbol("ref")); // error
```
