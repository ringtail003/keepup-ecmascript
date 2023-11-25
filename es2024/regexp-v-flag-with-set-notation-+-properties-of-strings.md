# RegExp v flag with set notation + properties of strings

正規表現でUnicode Character Propertiesが使えるようになった（\~ES2018）。\
\pに続けてシンボルを指定する。

```typescript
const re = /^\p{Emoji}$/u;

re.test("⚽"); // true
```

複数コードポイントからなる絵文字はチェックできなかった。

```typescript
re.test('👨🏾‍⚕️');
```

新しいシンボル追加により、複数コードポイントが指定できるようになった。

```typescript
const re = /^\p{RGI_Emoji}$/v;

re.test('👨🏾‍⚕️');
// true
```

### Hight Level API

正規表現の部分集合や差分が指定できるようになった。\
この指定はvフラグを付けて使用する。

```typescript
// 絵文字からASCIIを除く
[\p{Emoji}--\p{ASCII}]

/[\p{Emoji}--\p{ASCII}]/v.test("");
```

[https://zenn.dev/pixiv/articles/54e5d29c54e7f5](https://zenn.dev/pixiv/articles/54e5d29c54e7f5) が詳しい。

