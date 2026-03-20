# [Python](python_index.md)
## Streamlit
[Streamlit](https://docs.streamlit.io/)はPythonだけでWebアプリケーションを作成できるオープンソースフレームワーク

---

### モジュールの読み込み
```
import streamlit as st
```

---

### streamlit
#### 実行
```
streamlit run file_name.py
```

#### 設定されているパラメータとその値を確認する
```
streamlit config show
```

---

### サーバの設定
#### 設定ファイルの種類

- グローバル設定ファイル : 「~./streamlit/config.toml」 or 「%userprofile%/streamlit/config.toml」
- アプリケーション個別の設定ファイル : 実行するアプリケーションファイルと同じディレクトリ内の.streamlitディレクトリに配置する。「./.streamlit/config.toml」

#### 設定ファイル内のセクション
```
[global] : ----
[logger] : ログ
[client] : ----
[server] : サーバ
[mapbox] : ---
[theme] : テーマ
```


#config.tomlのテンプレート
```
[server]
address = "192.168.16.0"
port = 8080
sslCertFile =
sslKeyFile =
enableCORS = false
maxCacheSize = 2048
numThreads = 8
```

---