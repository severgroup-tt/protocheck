# Локальный запуск

Идёте в каталог где у вас лежат исходники вашего сервиса и выполняете:

```sh

$ docker run --rm -v $(pwd):/protos/protos --workdir /protos/protos ghcr.io/severgroup-tt/protocheck:latest
```

Все проверки запускаюся по умолчанию, если ошибки будут - вы узнаете, если нет - тоже :)

# Встраивание в github actions

Управление protocheck action осуществляется с помощью terraform (infra/tf/github/). По умолчанию работает на всех репозиториях, которые управляются из terraform.

Сам action находится в infra/tf/github/gh_files/protocheck.yaml
