# [Linux](linux_index.md)
## shell
### 設定ファイル
|file|description|
|-----|-----|
|/etc/profile|ログイン時に実行され、すべてのユーザから参照される|
|/etc/bash.bashrc|bash起動時に実行され、すべてのユーザから参照される|
|/etc/bashrc|`~/.bashrc`から参照されるファイル|
|~/.bash_profile|ログイン時に実行されるファイル|
|~/.bash_login|`~/.bash_profile`がない場合、ログイン時に実行されるファイル|
|~/.profile|`~/.bash_profile`、`~/.bash_profile`どちらもない場合、ログイン時に実行されるファイル|
|~/.bashrc|bash起動時に実行されるファイル|
|~/.bash_logout|ログアウト時に実行されるファイル|

---

### set
シェルのオプションを有効化/無効化するコマンド  
`-o`でオプションを有効化、`+o`でオプションを無効化する
```
set [-o/+o] [option]
```

|option|description|
|-----|-----|
|allexport|作成/変更した変数を自動的にエクスポートする|
|emacs|Emacs風のキーバインドにする|
|ignoreeof|<kbd> Ctrl </kbd> + <kbd> D </kbd>によってログアウトしないようにする|
|noclobber|出力リダイレクトによる上書きを禁止する|
|nolog|メタキャラクタを使ったファイル名を無効にする|
|vi|vi風のキーバインドにする|

#### 設定されているオプション一覧を確認する
```
set -o
```

---

### alias/unalias
エイリアスを設定/解除するコマンド
```
alias <alias_name>='<command>'
unalias <alias_name>
```

---

### function
関数を定義するコマンド
```
function
<function_name>
{
    <command>
}
```

---

### 複数コマンドの実行
|command|description|
|-----|-----|
|`<command> ; <command>`|左のコマンドを実行後、右のコマンドを実行する|
|`<command> && <command>`|左のコマンドが正常に終了したとき、右のコマンドを実行する|
|`<command> \|\| <command>`|左のコマンドが正常に終了しなかったとき、右のコマンドを実行する|
|`<command> \| <command>`|左のコマンドの出力結果をもとに、右のコマンドを実行する|

---

### 実行結果のファイルへの書き込み
|command|description|
|-----|-----|
|`<command> > output.txt`|実行結果をファイルに書き込む(新規作成/上書き)|
|`<command> >> output.txt`|実行結果をファイルに書き込む(追記)|

---

### ファイルからの読み込み
```
while IFS= read -r line; do
    echo "$line"
done < "input.txt"
```

---

### bashファイルの作成と実行
1. `hello.sh`を作成する
   ```
   #!/bin/bash

   echo "Hello!"
   ```
2. ファイルを実行する
   ```
   bash hello.sh
   ```

---

### 変数
#### 変数の扱い
````
# 代入
var1=text
var2=1234

# 変数の使用
$var1
"This product is ${var2} yen."
````

#### 特殊な変数
|variable|description|
|-----|-----|
|$0|スクリプトファイル名|
|$1, $2, $3|引数 ($1は1つ目の引数, $2は2つ目の引数)|
|$@|すべての引数 (スペース区切り)|
|$#|引数の数|
|$?|直前の処理の成否 (成功は0、失敗は0以外)|
|$$|シェルのPID|
|$RANDOM|0から32767の範囲の乱数を出力|

---

### 条件分岐
#### if文
```
if [ condition ] then
    <command>
elif [ condition ] then
    <command>
else
    <command>
fi
```

#### case式
```
case $var1 in
     1) <command> ;;
     2) <command> ;;
     *) <command> ;;
esac
```

#### 条件式
|condition|description|
|-----|-----|
|[-e\|-r\|-w\|-x] <file_name>/<directory_name>|ファイル/ディレクトリが [存在する|読み取り可能|書き込み可能|実行可能] かどうか|
|var1 [-eq\|-ne\|-lt\|-le\|-gt\|-ge] var2|var1とvar2が [等しい\|等しくない\|より小さい\|以下\|より大きい\|以上]
|! condition|条件を満たさない (NOT)|
|condition1 -a condition2|条件式1と条件式2の両方を満たす (AND)|
|condition1 -o condition2|条件式1と条件式2のどちらかを満たす (OR)|
|-n \<string\>|文字列の長さが0でない|

---

### 繰り返し処理
#### for文1 (0～10)
```
for var in $(seq 0 10)
do
    <command>
done
```

#### for文 (リスト)
```
for var in var1,var2,var3
do
    <command>
done
```

#### while文
```
while [ condition ]
do
    <command>
done
```

#### until文
```
until [ condition ]
do
    <command>
done
```

---