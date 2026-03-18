# [Linux](linux_index.md)
## job
### cron/atのアクセス制御ファイル
|file|description|
|-----|-----|
|/etc/cron.allow|cronの利用を許可するユーザを記述するファイル|
|/etc/cron.deny|cronの利用を拒否するユーザを記述するファイル|
|/etc/at.allow|atコマンドの利用を許可するユーザを記述するファイル|
|/etc/at.deny|atコマンドの利用を拒否するユーザを記述するファイル|

---

### crontab
crontabファイル(ジョブスケジュールを設定するファイル)を操作するためのコマンド
```
crontab [option]
```
|option|description|
|-----|-----|
|-e|エディタを使ってcrontabファイルを編集する|
|-l|crontabファイルの内容を表示する|
|-r|crontabファイルを削除する|
|-i|crontabファイルを削除時に確認する|
|-u <user_name>|ユーザを指定してcrontabファイルを編集する(rootユーザのみ使用可能)|

---

### at
1回限りのジョブをスケジューリングするためのコマンド
```
```

---

### at

---