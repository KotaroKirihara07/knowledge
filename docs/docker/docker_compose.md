# [Docker](docker_index.md)
## Docker Compose
### Docker Composeとは
Docker Composeとは、複数のコンテナを定義し実行する Docker アプリケーションのためのツール

---

### docker-compose.yml
[Compose file reference](https://docs.docker.com/reference/compose-file/)
#### [Services](https://docs.docker.com/reference/compose-file/services/)
???

|attribute|description|
|-----|-----|
|build|Dockerfileからイメージを生成してコンテナを生成する|
|image|`イメージ名:タグ名`の形式でイメージを指定してコンテナを生成する|
|ports|`"ホストのポート:コンテナのポート"`の形式でポートマッピングを行う|
|volumes||
|environment||
|||
|||
|||
|||
|||
|||
|||
|||

```
services:
  <service_name>:
    build: .
    ports:
      - "80:80"
    volumes:
      - aaa
    environment:
      - aaa
```

```
services:
  <service_name>:
    image: aaa
    ports:
      - "80:80"
    volumes:
      - aaa
    environment:
      - aaa
```

#### [Networks](https://docs.docker.com/reference/compose-file/networks/)
???

|attribute|description|
|-----|-----|
|attachable||
|driver||
|driver_opts||
|enable_ipv4||
|enable_ipv6||
|external||
|ipam||
|internal||
|labels||

```
networks:
  <front-tier>:
    attachable: aaa
    driver: aaaa
    driver_opts: aaa
    enable_ipv4: aaa
    enable_ipv6: aaa
    external: aaa
    ipam: aaa
    internal: aaa
    labels: aaa
```

#### [Volumes](https://docs.docker.com/reference/compose-file/volumes/)
???

|attribute|description|
|-----|-----|
|driver||
|driver opts||
|external||
|labels||
|name||

```
volumes:
  <volume_name>:
    driver: aaa
    driver_opts: aaa
    external: aaa
    labels: aaa
    name: aaa
```

#### [Configs](https://docs.docker.com/reference/compose-file/configs/)
???

|attribute|description|
|-----|-----|
|file|シークレットのパス|
|environment||
|content||
|external||
|name||

```
configs:
  http_config:
    file: ./httpd.conf
```

#### [Secrets](https://docs.docker.com/reference/compose-file/secrets/)
???

|attribute|description|
|-----|-----|
|file|シークレットのパス|
|environment|環境変数名|

```
secrets:
  server-certificate:
    file: ./server.cert
```

```
secrets:
  token:
    environment: "OAUTH_TOKEN"
```

---

### Docker Composeのコマンド
|command|description|
|-----|-----|
|`docker-compose up`|`docker-compose.yml`で定義されたコンテナを起動する|
|`docker-compose build`|`Dockerfile`から生成されるイメージを再構築する|
|`docker-compose ps`|Composeが管理しているコンテナの状態に関する情報を表示する|
|`docker-compose run`|単発のコマンドを実行するためにコンテナを起動する|
|`docker-compose logs`|Composeが管理しているコンテナのログを表示する|
|`docker-compose stop`|コンテナを停止する|
|`docker-compose rm`|停止しているコンテナを削除する|

> 参考資料  
> [docker compose (日本語版)](https://docs.docker.jp/engine/reference/commandline/compose.html)  
> [docker compose (英語版)](https://docs.docker.com/reference/cli/docker/compose/)  

---