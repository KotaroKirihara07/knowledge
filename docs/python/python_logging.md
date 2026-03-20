# [Python](python_index.md)
## logging
[logging](https://docs.python.org/ja/3/library/logging.html)はアプリケーションやライブラリのための柔軟なエラーログ記録 (logging) システムを実装するためのモジュール

---

### モジュールの読み込み
```
import logging
```

---

### ログ
#### ログレベル
|level|description|
|-----|-----|
|critical||
|error||
|warning||
|info||
|debug||

#### ロガーの設定
```
logging.basicConfig(
    level=logging.DEBUG,
    format="%(message)s",
    datefmt="[%X]",
    handlers=[logging.FileHandler(filename="./log.txt")]
)
```

#### ログレベルを変更
```
logging.setLevel(logging.DEBUG)
```

#### モジュールレベルのロガーの作成
```
logger = logging.getLogger(__name__)
```

#### ログ出力
```
logger.critical("message")
logging.error("message")
logging.warning("message")
logging.info("message")
logging.debug("message")
```

---