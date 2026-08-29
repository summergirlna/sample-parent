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
$ docker compose --profile batch run --rm batch run.id=1

# フォーマッタ・Linter実行
$ ./mvnw verify

# フォーマッタ適用
$ ./mvnw spotless:apply
```

## rabbitmq

バッチ実行前にキューにメッセージを入れておく必要がある。

content_type = application/json

```json
{
  "requestId": "report-001",
  "userIds": [
    "48fa5817-2d5d-481a-b5a1-24ce52f60a1f"
  ]
}
```