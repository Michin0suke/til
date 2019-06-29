# Linuxコマンド

## wc (word count)
行数を数える

## sort
ソートする。
オプション
* -r : 逆順

## uniq
重複した行を削除、あるいは重複した行を表示する。

## ログの表示

sudo cat /var/log/secure | grep "Jun 23 .* Failed password for invalid user" | awk -F' ' '{print $11}' | sort

## ssh
sshでパスワード認証を指定する方法
ssh username@ipaddress -o PreferredAuthentications=password

### カウント
sudo cat /var/log/secure | grep "Jun 23 .* Failed password for invalid user" | awk -F' ' '{print $11}' | sort | uniq > invalid_user.txt

sudo cat /var/log/secure | grep "Jun 23 .* Failed password for invalid user" | awk -F' ' '{print $13}' | sort > invalid_ports.txt

sudo cat /var/log/secure | grep "Jun 23 .* Failed password for invalid user .* port 22" | head