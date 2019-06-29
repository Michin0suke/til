#ダウンロード系

### wget

なかったらインストール

```sh
$ yum install wget
```

oオプションでインストール先を指定できる

```
$ wget -O [インストール先] [インストール元のURL]
```

### 解凍/圧縮

[参考](https://qiita.com/supersaiakujin/items/c6b54e9add21d375161f)

圧縮
```sh
tar -zcvf xxxx.tar.gz directory
```

解凍
```sh
tar -zxvf xxxx.tar.gz
```