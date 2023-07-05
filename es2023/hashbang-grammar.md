# Hashbang Grammar

シェルスクリプトなどで見る先頭 `#!` で始まる行をShebangと呼ぶ。\
自身を実行するインタプリタを指定するもの。

Nodeでも使えるようになった。

```typescript
#!/usr/bin/env node

export {};
console.log("Hello");
```

Shebangと呼ばずHashbangとしているのは `#` がハッシュタグとして呼ばれているから、らしい。
