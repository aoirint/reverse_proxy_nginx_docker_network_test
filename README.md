# reverse_proxy_nginx_docker_network_test

リバースプロキシ用のnginxをdocker-composeで管理するテスト。

仮想アプリプロジェクトの起動。

```shell
cd app_project
docker-compose up -d
```

仮想nginxプロジェクトの起動。

```shell
cd nginx_project
docker-compose up -d
```

ホストの`/etc/hosts`に`app.example.com`を追記。

```
127.0.0.1 app.example.com
```

ブラウザで`app.example.com`にアクセスすると、仮想アプリの80番ポートにリクエストが飛ぶ。
