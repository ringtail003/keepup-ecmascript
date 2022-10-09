# Private fields in-in

メソッドの引数に関して、特定のプライベートフィールドを持つかどうか `in` 演算子で判定できるようになった。

この機能がない場合、try...catchで例外を使った冗長な書き方を使うしかない。もっとシンプルに書きたいというモチベーションで提案された。

```javascript
class Parent {
  #type = "dummy";

  static isFamily(obj) {
    // もっとシンプルに書きたい
    try {
      obj.#type;
    } catch() {
      return false;
    }
    return true;
  }
}
```

### Example

```javascript
class Parent {
  #type = "dummy";

  static isFamily(obj) {
    return #type in obj;
  }
}
console.log(Parent.isFamily(new Parent())); // true

// 継承した子クラスも判定できる
class Child extends Parent {}
console.log(Parent.isFamily(new Child()));
```

### Link

{% embed url="https://github.com/tc39/proposal-private-fields-in-in" %}

{% embed url="https://caniuse.com/mdn-javascript_classes_private_class_fields_in" %}

{% embed url="https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Classes/Private_class_fields#%E3%83%97%E3%83%A9%E3%82%A4%E3%83%99%E3%83%BC%E3%83%88%E3%82%A4%E3%83%B3%E3%82%B9%E3%82%BF%E3%83%B3%E3%82%B9%E3%83%95%E3%82%A3%E3%83%BC%E3%83%AB%E3%83%89" %}
