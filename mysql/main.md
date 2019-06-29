maradbはここからダウンロードする

https://www.softwarecollections.org/en/scls/rhscl/rh-mariadb102/



mariadb-serverもインストールする



### すでにあるカラムにユニーク属性を追加する

```sql
alter table contents add unique (link)
```

### すでにあるカラムの型を変更する

```sql
ALTER TABLE [テーブル名] MODIFY [カラム名] [型] NOT NULL;
```

### テーブルの詳細を得る

```sql
DESC `users`;
SHOW COLUMNS FROM `users`;
```

### ユーザの確認

```sql
SELECT user,host,password FROM mysql.user;

SHOW GRANTS FOR root@'localhost';
```

### ユーザを作成する

```sql
create user 'user'@'localhost' identified by 'password';
```

### ユーザを削除する

```sql
drop user user@localhost;
```

### 権限を付与する

```sql
GRANT ALL ON testdatabase.* TO user@'%' IDENTIFIED BY 'password';
```
%はどのホストからでも接続できる

### データの場所を確認する

```bash
locate my.cnf
```


### エクスポート

データベースを吐き出す場合
```sql
mysqldump -u USER_NAME -p -h HOST_NAME DB_NAME > OUTPUT_FILE_NAME
#example
mysqldump -uroot -ppassword -hlocalhost prizz > prizz.dump.sql
```