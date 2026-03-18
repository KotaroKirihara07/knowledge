# [Linux](linux_index.md)
## user/group
### 基本的なファイル
|file|description|
|-----|-----|
|/etc/passwd|ユーザ情報が保存されているファイル|
|/etc/shadow|パスワード情報が保存されているファイル|
|/etc/group|グループ情報が保存されているファイル|
|/etc/default/useradd|useraddコマンドのデフォルト値が保存されているファイル|

---

### useradd
ユーザを追加するためのコマンド
```
useradd [option] <user_name>
```

|option|description|
|-----|-----|
|-c <comment> |コメントフィールドを指定する|
|-d <path>|ホームディレクトリを指定する|
|-g <group_name/GID>|主グループを指定する|
|-G <group_name>/<GID>|補助グループ名を指定する|
|-s <path>|デフォルトシェルを指定する|
|-D|デフォルトの設置値を表示/設定する|
|-m|ホームディレクトリを自動的に作成する|

---

### usermod
ユーザの設定を編集するためのコマンド
```
usermod [option] <user_name>
```

|option|description|
|-----|-----|
|-c <comment> |コメントフィールドを指定する|
|-d <path>|ホームディレクトリを指定する|
|-g <group_name/GID>|主グループを指定する|
|-G <group_name>/<GID>|補助グループ名を指定する|
|-s <path>|デフォルトシェルを指定する|
|-L|パスワードをロックして一時的に無効化する|
|-U|パスワードのロックを解除する|

---

### userdel
ユーザを削除するためのコマンド
```
userdel [option] <user_name>
```

|option|description|
|-----|-----|
|-r|ホームディレクトリも含めて削除する|
|-f|ログイン中のユーザを削除する|

---

### passwd
ユーザのパスワードを変更するためのコマンド
```
passwd [option] <user_name>
```

|option|description|
|-----|-----|
|-l|パスワードをロックして一時的に無効化する|
|-u|パスワードのロックを解除する|

---

### groupadd
グループを作成するためのコマンド
```
groupadd [option] <group_name>
```

|option|description|
|-----|-----|
|-g <GID>|グループIDを指定する|

---

### groupmod
グループの設定を編集するためのコマンド
```
groupmod [option] <group_name>
```

|option|description|
|-----|-----|
|-g <GID>|グループIDを指定する|
|-n <group_name>|グループ名を変更する|

---

### groupdel
グループを削除するためのコマンド
```
groupdel <group_name>
```

> [!CAUTION]
> 削除対象グループをプライマリグループとするユーザが存在する場合、グループの削除に失敗する

---

### id
ユーザの情報を表示するためのコマンド
```
id [option] <user_name>
```

|option|description|
|-----|-----|
|-u|ユーザIDを表示する|
|-g|グループIDを表示する|
|-G|補助グループを含むグループIDを表示する|
|-n|ユーザID、グループID、補助グループIDを表示する|

---



