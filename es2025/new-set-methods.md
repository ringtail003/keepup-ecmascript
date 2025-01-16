# New Set Methods

{% embed url="https://github.com/tc39/proposal-set-methods" %}

## TL;DR

Setのメソッドが拡張された。

```typescript
// AND
new Set([1, 2]).intersection( new Set([1, 3])); // {1}

// OR
new Set([1, 2]).union( new Set([1, 3])); // {1, 2, 3}

// 差集合
new Set([1, 2]).difference( new Set([1, 3])); // {2}

// XOR
new Set([1, 2]).symmetricDifference( new Set([1, 3])); // {2, 3}

// 部分集合
new Set([1]).isSubsetOf( new Set([1, 2])); // true

// isSubsetOfの逆
new Set([1, 2]).isSupersetOf( new Set([1])); // true

// 共通点がない
new Set([1, 2]).isDisjointFrom(new Set([3, 4])); // true
```
