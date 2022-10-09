# Regexp match indices

{% embed url="https://github.com/tc39/proposal-regexp-match-indices" %}

`d` フラグを付けて正規表現で検索した場合に、マッチした位置を `indices` から得られるようになった。

### Example

```javascript
const text = "abc-abc*abc/abc";
const regex = /(?<text>abc)/dg;

for (match of text.matchAll(regex)) {
  console.log(match);
  // { indices: { groups: { text: [0,4] } } }
  // { indices: { groups: { text: [4,7] } } }
  // { indices: { groups: { text: [8,11] } } }
  // { indices: { groups: { text: [12,15] } } }
}
```

### Link

{% embed url="https://caniuse.com/mdn-javascript_builtins_regexp_hasindices" %}

{% embed url="https://developer.mozilla.org/ja/docs/Web/JavaScript/Guide/Regular_Expressions#%E3%83%95%E3%83%A9%E3%82%B0%E3%82%92%E7%94%A8%E3%81%84%E3%81%9F%E9%AB%98%E5%BA%A6%E3%81%AA%E6%A4%9C%E7%B4%A2" %}
