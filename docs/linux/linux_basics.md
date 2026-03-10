# [Linux](linux_index.md)
## basics
### ディストリビューション
主なLinuxのディストリビューションは「Red Hat系」、「Debian系」の2種類存在する。
#### Red Hat系
- Red Hat Enterprise Linux
- Cent OS / Cent OS Stream
- Fedora
- Alma Linux

#### Debian系
- Debian GNU/Linux
- Ubuntu

> [!NOTE]
> Amazon LinuxはRed Hat系/Debian系のどちらか明らかにされていないらしい。

---

### ユーザ
Linuxにおけるユーザは「rootユーザ」、「一般ユーザ」に分けられる。
- rootユーザ : システム管理が可能なユーザ。
- 一般ユーザ : 操作に制限があるユーザ。

---

### 基本的なディレクトリ構造
|path|usage|
|-----|-----|
|/etc|設定ファイル用|
|/home|一般ユーザ用のホーム|
|/root|rootユーザ用のホーム|
|/boot|起動に関するファイル用|
|/bin|一般ユーザが実行可能なファイル用|
|/sbin|ルートユーザが実行可能なファイル用|
|/lib|ライブラリファイル用|
|/proc|プロセスやカーネルについてファイル用|
|dev|デバイスファイル用|
|/usr|インストールされたプログラムやコマンドに関するファイル用|
|/var|ログファイルやWeb公開用のドキュメント用|
|/tmp|一時的なファイル用|
|/mnt|ファイルシステム用のマウントポイント用|
|/media|メディアファイルのマウントポイント用|

---

### 基本的なファイル
|path|usage|
|-----|-----|
|||
|||
|||
|||
|||
|||
|||
|||
|||
|||
|||
|||

---

### man
オンラインマニュアルを表示するためのコマンド
```
man [option] <section> <keyword>
```

---

### hisotriy
コマンドの履歴を表示するためのコマンド
```
hisotriy [option]
```

---

### コマンドの実行結果のファイルへの書き込み
#### 標準出力をファイルに上書きする
```
*command* > outputs.txt
```

#### 標準出力をファイルに追記する
```
*command* >> outputs.txt
```

#### コマンド実行時のすべての出力結果をファイルに上書きする
```
*command* &> outputs.txt
```

#### コマンド実行時のすべての出力結果をファイルに追記する
```
*command* &>> outputs.txt
```

---


