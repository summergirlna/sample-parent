## docker

```shell
$ docker compose up --build

# ボリューム作り直し
$ docker compose down -v
```

## maven

```shell
# 負荷ツール実行
$ ./mvnw -pl sample-loadtest gatling:test
```