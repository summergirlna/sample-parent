## docker

```shell
# 通常起動(インフラサービスを外部公開しない)
$ docker compose up --build

# デバッグ起動(インフラサービスを外部公開する)
$ docker compose -f docker-compose.yaml -f docker-compose.debug.yaml up --build

# ボリューム作り直し
$ docker compose down -v
```

## maven

```shell
# 負荷ツール実行
$ ./mvnw -pl sample-loadtest gatling:test

# バッチビルド
$ docker compose --profile batch build batch

# バッチ実行(MQ投入)
$ docker compose --profile batch run --rm batch --spring.batch.job.name=userNameListReportRequestJob run.id=$(date +%Y%m%d%H%M%S) request.id=report-002 user.ids=48fa5817-2d5d-481a-b5a1-24ce52f60a1f

# バッチ実行(MQ刈り取り)
$ docker compose --profile batch run --rm batch --spring.batch.job.name=userNameListReportJob run.id=$(date +%Y%m%d%H%M%S)

# フォーマッタ・Linter実行
$ ./mvnw verify

# フォーマッタ適用
$ ./mvnw spotless:apply
```
