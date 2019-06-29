# sshd_configの設定

```
#PasswordAuthentication yes
↓
PasswordAuthentication no
```
```
#RSAAuthentication yes
　　　　　　　↓
RSAAuthentication yes　←RSA認証を許可（ssh1のみ）
```
```
#PubkeyAuthentication yes
　　　　　　　↓
PubkeyAuthentication yes　←公開鍵認証を許可（ssh2のみ）
```
```
#RhostsAuthentication no
　　　　　　　↓
RhostsAuthentication no　←rhost認証を禁止
```