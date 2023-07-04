# Private class fields

完全にカプセル化されたプライベートフィールド・プライベートメソッドが宣言できるようになった。

TypeScriptのprivateアクセサを使った場合、トランスパイル後のJavaScriptではむき出しのフィールド・メソッドに変換され、privateはTypeScriptで開発している時だけの保護機能として存在する（ソフトプライベート）。

新しく提案された「Private class fields」はJavaScript上でもカプセル化を実現できるため、完全な保護機能を持つ（ハードプライベート）。

### Example

プライベートフィールド・プライベートメソッドを宣言した例。

```javascript
class Foo {
  #value = 1;
  #fetch() {}
}

const foo = new Foo();

foo.#value; // Error!
foo.#fetch(); // Error!
```

staticブロックも導入された。クラスが評価される時に一度だけ実行されるブロックで、外部からリソースを取得し自身のフィールドを初期化する時などに使える。

```javascript
class Foo {
  static x;
  static y;
  static {
    this.x = this.y;
  }
}
```

### Link

{% embed url="https://github.com/tc39/proposal-class-fields" %}

{% embed url="https://caniuse.com/mdn-javascript_classes_private_class_fields" %}

{% embed url="https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Classes/Private_class_fields" %}
