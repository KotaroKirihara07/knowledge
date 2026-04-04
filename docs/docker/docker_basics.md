# [Docker](docker_index.md)
## basics
### Dockerfileを使用したコンテナの作成
一つのコンテナ(一つのサービス)を構築する場合、`Dockerfile`を使用すると便利。
1. `Dockerfil`eを作成する
2. `docker build`コマンドでDockefileからでDockerイメージを作成する
3. `docker container run`コマンドでコンテナを作成する
4. `docker container stop`コマンドでコンテナを停止する
5. `docker container rm`コマンドでコンテナを削除する

---

### Docker Composeを使用したコンテナの作成
複数のコンテナ(複数のサービス)を構築する場合、`Dockerfile`+`compose.yml`を使用すると便利。
1. `Dockefile`を作成する
2. `docker-compose.yaml`を作成する
3. `docker-compose up`コマンドでコンテナを作成する
4. `docker-compose stop`コマンドでコンテナを停止する
5. `docker-compose rm`コマンドでコンテナを削除する

---
