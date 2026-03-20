# [Python](python_index.md)
## tomllib
[tomllib](https://docs.python.org/ja/3/library/tomllib.html)はtomlファイルを扱うためモジュール

---

### モジュールの読み込み
```
import tomllib
```

---

### ファイルの操作
#### tomllibファイルの読み込み
```
with open(file_path, mode="r") as f:
    data = tomllib.load(f)
username = data["default"]["name"]
```

#### tomllibファイルへの書き込み
```
with open(file_path, mode="w") as f:
    data = tomllib.load(f)
    data["default"]["age"] = 20
    toml.write(data)
```

---