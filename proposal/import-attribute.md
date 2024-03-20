# Import Attribute

{% embed url="https://github.com/tc39/proposal-import-attributes" %}

## TL;DR

import文のMIMEタイプ指定がサポートされた。

## Usage

```typescript
import json from "./foo.json" with { type: "json" };

// Dynamic import
import("foo.json", { with: { type: "json" } });
```

type以外にもメタデータを渡せるよう。

```typescript
import value from "module" with { attr: { key1: "value1" } };
```
