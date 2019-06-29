docker-compose

`nginx.conf`は直接volumesに指定しないとうまく動作しない

これだとダメ

```
nginx:
  volumes:
    - ./nginx:/etc/nginx:ro
```
これだとOK

```conf
nginx:
  volumes:
    - ./nginx/nginx.conf:/etc/nginx/nginx.conf:ro
    - ./nginx/conf.d:/etc/nginx/conf.d:ro
```

ファイル構成

```
docker
`-- nginx
    |-- conf.d
    |   `-- default.conf
    `-- nginx.conf

```





### コマンド

```
docker ps -a
docker volume ls
```



```
docker-compose rm -v
docker-compose down -v
docker volume prune
# ダメなとき
docker-compose down -v --remove-orphans
```

```
# とりあえずコンテナを全部止める
$ docker-compose down

$ docker volume ls
# たくさんのVolumeが出てきた、エラーでストレージがなんとかかんとか言ってるので全部削除
$ sudo docker volume rm $(sudo docker volume ls -qf dangling=true)
```

$ docker-compose up --build を実行したら起動しました。



docker inspect [volume]



```sh
mysql -h 127.0.0.1 -P 3306 -u root -p
```



```
docker exec -it sample-project_db_1 bash
```

[コマンド一覧](https://qiita.com/wasanx25/items/d47caf37b79e855af95f#down)





```
web:
    links:
        - php
```

`links:` を設定することで、nginx のコンテナの　`/etc/hosts` にサービス情報が追加されます。これにより、`site.conf` に以下のように記載することができます。

```
fastcgi_pass php:9000;
```