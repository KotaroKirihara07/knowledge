# [Docker](docker_index.md)
## Docker Compose
### Docker Composeとは


---

### docker-compose.yml
[Compose file reference](https://docs.docker.com/reference/compose-file/)
#### [Services](https://docs.docker.com/reference/compose-file/services/)
???

|attribute|description|
|-----|-----|
|image||
|ports||
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
    image: aaa
    ports:
      - 80:80
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