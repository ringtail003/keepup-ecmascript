# Import Attributes

{% embed url="https://github.com/tc39/proposal-import-attributes" %}

## TL;DR

import文のMIMEタイプ指定がサポートされた。

## Usage

```typescript
import json from "./foo.json" with { type: "json" };
import styles from "./styles.css" with { type: "css" };
```

属性を拡張してメタデータを渡せるようになったと記載がある。\
用途不明。

```typescript
import value from "module" with { attr: { key1: "value1" } };
```

ダイナミックインポートの場合は以下のように記述する。

```typescript
import("foo.json", { with: { type: "json" } });
```
