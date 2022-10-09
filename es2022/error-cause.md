# Error cause

### GitHub

{% embed url="https://github.com/tc39/proposal-error-cause" %}

### Overview

エラーを追跡するための `cause` が使えるようになった。

### Example

```javascript
try {
  render();
} catch (e) {
  // (4) キャッチする
  // causeを使わない場合、一番上でラップしている "renderでエラー" しか取れない
  console.log("エラー", e.cause);
}

function render() {
  try {
    load();
  } catch(e) {
    // (3) 伝播する
    throw new Error("renderでエラー", { cause: e });
  }
}
function load() {
  try {
    fetch();
  } catch(e) {
    // (2) 伝播する
    throw new Error("loadでエラー", { cause: e });
  }
}
function fetch() {
  try {
    throw new Error("Invalid URL");
  } catch(e) {
    // (1) ここでエラーが発生する
    throw new Error("fetchでエラー", { cause: e });
  }
}
```

### Appendix

### Document

{% embed url="https://caniuse.com/mdn-javascript_builtins_error_cause" %}

{% embed url="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error/cause" %}
