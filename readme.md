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

# バッチ実行
$ docker compose --profile batch build batch
$ docker compose --profile batch run --rm batch ids=0db8dd77-8a54-4eea-91a7-d0808ee22385_0f84f7b6-1853-42c3-8b4d-896b497a0f31 run.id=1
```