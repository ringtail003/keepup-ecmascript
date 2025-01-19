# RegExp Modifiers

{% embed url="https://github.com/tc39/proposal-regexp-modifiers" %}

## TL;DR

正規表現のパターン修飾子（i、m、s）が文全体でなく、部分的に適用できるようになった。

```typescript
// 全体：abいずれが大文字小文字でもOK
/^AB$/i
```

```typescript
// 部分適用：bの部分が大文字小文字どちらでもOK
/^A(?i:B)$/test("Ab") // true
/^A(?i:B)$/test("aB") // false
```

```typescript
// 部分適用（打ち消し）
/^A(?-i:B)$/i.test("aB") // true
/^A(?-i:B)$/i.test("ab") // false
```

g、y、u、dには適用できない。
