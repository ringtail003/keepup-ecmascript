# Top-level await

{% embed url="https://github.com/tc39/proposal-top-level-await" %}

関数宣言や関数式の外（モジュールのトップレベル）でasyncなしのawaitが使えるようになった。

### Example

```javascript
<script type="module">
  const result = await fetch("https://...");
</script>
```

### Link

{% embed url="https://caniuse.com/mdn-javascript_operators_await_top_level" %}

{% embed url="https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/await" %}
