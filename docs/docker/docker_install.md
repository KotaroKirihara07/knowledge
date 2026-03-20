# [Docker](docker_index.md)
## Install
### Docker Engine
#### Ubuntu
1. apt パッケージのインデックスを更新する
   ```
   sudo apt-get update
   ```
2. Docker をインストールする
   ```
   sudo apt-get install docker-engine
   ```
3. Docker のバージョンを確認する
   ```
   docker version
   ```
4. docker デーモンを開始する
   ```
   sudo systemctl start docker
   ```
5. docker デーモンの状況を確認する
   ```
   systemctl status docker
   ```


---

### Docker Compose

---