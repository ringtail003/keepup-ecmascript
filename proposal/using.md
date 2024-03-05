# using

## TL;DR

`using` による変数宣言が導入された。\
スコープ外になる前にリソースの解放が行われる。

DBコネクション、ファイル読み込みなど、外部リソースの解放をハンドリングできるようになった。

## Example - sync

従来のリソース解放の例

```javascript
const db = new DB();

try {
    db.query("SELECT ...");
} finally {
    db.close();
}
```

usingを関数で使用した例

```javascript
function createDB() {
    const db = new DB();
    
    return {
        db,
        [Symbol.dispose]: () => db.close(),
    };
}
```

usingをクラスで使用した例

```javascript
class DBConnection {
    #db = new DB();
    
    [Symbol.dispose]: () => {
        this.#db.close();
    }
}
```

## Example - async

```javascript
function createDB() {
    const db = new DB();
    
    return {
        db,
        [Symbol.asyncDispose]: async () => db.close(),
    };
}

class DBConnection {
    #db = new DB();
    
    async [Symbol.asyncDispose]() {
        this.#db.close();
    }
}
```
