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
$ docker compose --profile batch run --rm batch ids=24fc789e-fb47-45bd-b741-a6bbd9a8b3cd_2e7f9ccd-9842-4ba8-9a33-988db13f0c22 run.id=1
```