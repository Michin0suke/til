###インストール

```sh
echo "export GOPATH=$HOME/go" >> ~/.bash_profile
echo "alias gogo='cd $GOPATH/src/github.com/Michin0suke/'" >> ~/.bash_profile
source ~/.bash_profile
```

```sh
go get -u golang.org/x/lint/golint
go get -u github.com/gin-gonic/gin
go get -u github.com/go-sql-driver/mysql

```