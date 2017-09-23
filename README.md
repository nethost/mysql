# Mysql Docker Images

Docker + Alpine + Mysql 

#### Parameter
- `MYSQL_ROOT_PWD` : root Password default "mysql"
- `MYSQL_USER` : new User
- `MYSQL_USER_PWD` : new User Password
- `MYSQL_USER_DB` : new Database for new User

#### Run a default container
```
$ docker run --name mysql -v /Users/billgo/data/mysql:/var/lib/mysql -d -p 3306:3306 nethost/mysql
```

#### Run a container with new User and Password
```
$ docker run --name mysql -v /Users/billgo/data/mysql:/var/lib/mysql -d -p 3306:3306 -e MYSQL_ROOT_PWD=123456 -e MYSQL_USER=billgo -e MYSQL_USER_PWD=123456 nethost/mysql
```

#### Run a container with new Database for new User and Password
```
$ docker run --name mysql -v /Users/billgo/data/mysql:/var/lib/mysql -d -p 3306:3306 -e MYSQL_ROOT_PWD=123456 -e MYSQL_USER=billgo -e MYSQL_USER_PWD=123456 -e MYSQL_USER_DB=default nethost/mysql
```