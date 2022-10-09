# Class static block

{% embed url="https://github.com/tc39/proposal-class-static-block" %}

クラス構文のstaticなフィールド・メソッド・ブロックが使えるようになった。

従来では動的にクラスの変数を追加することで実現していたが、よりクラスらしい宣言ができるようになった。

```javascript
// 従来
class LegacyWay {}
LegacyWay.value = "";
```

### Link

```javascript
class Foo {
  static url;
  static #prefix = "/api";
  static {
    this.url = `${this.#y}/users`;
  }
}
console.log(Foo.url); // "/api/users"
```

{% embed url="https://caniuse.com/mdn-javascript_classes_static" %}

{% embed url="https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Classes/static" %}
