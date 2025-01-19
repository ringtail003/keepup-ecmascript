# Duplicate named capture groups

## TL;DR

名前付きキャプチャグループで、同じ名前を複数回書けるようになった。

```typescript
"2025-01-02".match((?<year>\d{4})-\d{2}|-\d{2}-(?<year>\d{4})/) > "2025"
"01-02-2025".match((?<year>\d{4})-\d{2}|-\d{2}-(?<year>\d{4})/) > "2025"
```
