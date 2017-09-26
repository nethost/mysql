# Mysql Docker Images

Docker + Alpine + Mysql5.7

#### Parameter
- `MYSQL_USER` : new User
- `MYSQL_PASSWORD` : new User Password
- `MYSQL_DATABASE` : new Database for new User
- `MYSQL_ROOT_PASSWORD` : root Password default "mysql"

#### Run a default container
```
$ docker run --name mysql -v /Users/billgo/data/mysql:/var/lib/mysql -d -p 3306:3306 nethost/mysql
```

#### Run a container with new User and Password
```
$ docker run --name mysql -v /Users/billgo/data/mysql:/var/lib/mysql -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 -e MYSQL_USER=billgo -e MYSQL_PASSWORD=123456 nethost/mysql
```

#### Run a container with new Database for new User and Password
```
$ docker run --name mysql -v /Users/billgo/data/mysql:/var/lib/mysql -d -p 3307:3306 -e MYSQL_ROOT_PASSWORD=123456 -e MYSQL_USER=billgo -e MYSQL_PASSWORD=123456 -e MYSQL_DATABASE=default nethost/mysql:5.7
```

## 辅助命令
```
$ docker ps -l
$ docker stop $(docker ps -a -q)
$ docker rm $(docker ps -a -q)
$ docker rmi $(docker images -q)
$ docker rmi $(docker images -q -f dangling=true)
```