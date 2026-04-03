# [Docker](docker_index.md)
## Dockerfile
### Dockerfileの命令

|Instruction|Description|
|-----|-----|
|`ADD`|ビルドコンテクストやリモートのURLからイメージへファイルをコピーする|
|`ARG`|docker buildする際に指定できる引数を宣言する|
|`CMD`|コンテナ起動後に指定された命令を実行する|
|`COPY`|ファイルやディレクトリをコピーする|
|`ENTRYPOINT`|コンテナの起動時に実行する実行可能ファイルとデフォルト引数を指定する|
|`ENV`|環境変数を設定する|
|`EXPOSE`|プロセスの接続ポートを指定する|
|`FROM`|ベースイメージを指定する|
|`HEALTHCHECK`|ヘルスチェックの方法をカスタマイズする|
|`LABEL`|イメージにラベルを付与する|
|`MAINTAINER`|イメージのAuthorメタデータに指定された文字列を設定する|
|`ONBUILD`|他のイメージのベースイメージとして呼び出されたときに実行される命令を指定する|
|`RUN`|ビルドコマンドを実行する|
|`SHELL`|ビルド時のシェルを指定する|
|`STOPSIGNAL`|docker stopする際に、コンテナで実行しているプログラムに対して送信するシグナルを変更する|
|`USER`|ユーザやグループIDを設定する|
|`VOLUME`|ボリュームマウントを作成する|
|`WORKDIR`|ワーキングディレクトリを変更する|

> 参考資料  
> [Dockerfile リファレンス](https://docs.docker.jp/engine/reference/builder.html)  
> [Dockerfile reference](https://docs.docker.com/reference/dockerfile/)

---

### ベースイメージ
#### Linuxのイメージ
|image|description|
|-----|-----|
|ubuntu|Ubuntu|
|centos|CentOS|
|debian|DebianOS|
|fedora|Fedora|
|busybox|BizyBox|
|alpine|Alpine linux|

#### Webサーバやデータベースサーバのイメージ
|image|description|
|-----|-----|
|httpd|Apache|
|nginx|Nginx|
|mysql|MySQL|
|postgres|PostgreSQL|
|mariadb|MariaDB|
|wordpress|WordPress (MySQLまたはMariaDBが必要)|
|nextcloud|NextCloud|
|redmine|Redmine (PostgreSQLまたはMySQLが必要)|
|registry|Dockerレジストリ|


#### プログラミング言語のイメージ
|image|description|
|-----|-----|
|openjdk|Javaの実行環境|
|[python](https://hub.docker.com/_/python)|Pythonの実行環境|
|php|PHPの実行環境|
|ruby|Rubyの実行環境|
|perl|Perlの実行環境|
|gcc|C/C++コンパイラ|
|node|Node.js|

---