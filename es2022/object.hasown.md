# Object.hasOwn

{% embed url="https://github.com/tc39/proposal-accessible-object-hasownproperty" %}

オブジェクトの `hasOwn` が使えるようになった。 従来の `hasOwnProperty` は外部で書き換えられるため、安全のために `Object.prototype.hasOwnProperty().call` を使うケースがあったが、これと同じことができるようになった。

### Example

```javascript
const obj = { value:1 };
Object.hasOwn(obj, "value");
// true
```

### Link

{% embed url="https://caniuse.com/mdn-javascript_builtins_object_hasown" %}

{% embed url="https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwn" %}
