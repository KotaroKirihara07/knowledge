# [Linux](linux_index.md)
## system
### systemctl
サービスやシステムのユニットを管理・制御するためのコマンド
```
systemctl <subcommand> <target>
```
|subcommand|description|
|-----|-----|
|get-default|システム起動時のデフォルトターゲットを表示する|
|set-default|システム起動時のデフォルトターゲットを変更する|
|isolate|???|

|target|description|
|-----|-----|
|multi-user.target|CUIログイン|
|graphical.target|グラフィカルログイン|
|poweroff.target|システム終了|
|rescue.target|レスキューモード|
|reboot.target|システム再起動|

---

### shutdown
シャットダウンを実行するためのコマンド
```
shutdown [option] <time> <"message">
```

|option|description|
|-----|-----|
|-c|実行中のシャットダウンをキャンセルする|
|-f|次回起動時にfsckをスキップする (-h/-r と併用する)|
|-F|次回起動時にfsckを必ず実行する (-h/-r と併用する)|
|-h|シャットダウン|
|-k|警告メッセージのみ通知する|
|-r|シャットダウン後に再起動|

---