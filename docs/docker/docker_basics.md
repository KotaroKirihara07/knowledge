# [Docker](docker_index.md)
## basics
### Dockerfileを使用したコンテナの作成
一つのコンテナ(一つのサービス)を構築する場合、`Dockerfile`を使用すると便利。
1. `Dockerfile`を作成する
2. `docker build`コマンドでDockefileからでDockerイメージを作成する
3. `docker container run`コマンドでコンテナを作成する
4. `docker container stop`コマンドでコンテナを停止する
5. `docker container rm`コマンドでコンテナを削除する

#### `docker container run` コマンド例
ポート開放とボリュームを使用を行う場合、`-p`と`-v`は必須。その他のオプションはDockerfileの内容を上書きするために使用する。

```
docker container run -d \
  -p 80:80 \
  -v /host/data:/data \
  -e <key>=<value> \
  --name <contaner_name> \
  <image_name>
```

---

### Docker Composeを使用したコンテナの作成
複数のコンテナ(複数のサービス)を構築する場合、`Dockerfile`+`compose.yml`を使用すると便利。
1. `Dockefile`を作成する
2. `docker-compose.yaml`を作成する
3. `docker-compose up`コマンドでコンテナを作成する
4. `docker-compose stop`コマンドでコンテナを停止する
5. `docker-compose rm`コマンドでコンテナを削除する

#### `docker-compose up` コマンド例

```
docker-compose up -d
```

---

### Docker Hub
[Docker Hub](https://www.docker.com/ja-jp/products/docker-hub/)はDocker Inc.が提供しているオンラインレジストリ。

---


### Docker Registry
ローカルで動作可能なオープンソースのアプリケーション。

---
