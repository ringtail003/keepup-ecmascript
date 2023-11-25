# Well-Formed Unicode Strings

UTF-16のサロゲートペアのための文字列検証をするメソッドらしい。

```typescript
"\uD867\uDE3D".isWellFormed();
// 上位サロゲート+下位サロゲート true

"𩸽".isWellFormed();
// 文字列 true

"\u{29e3d}".isWellFormed();
// コードポイント true
```

[https://zenn.dev/link/comments/c1da8dd5306e1d](https://zenn.dev/link/comments/c1da8dd5306e1d)

toWellFormedも入ってくるみたい。

```typescript
"\u{29e3d}".toWellFormed();
// "𩸽"
```
