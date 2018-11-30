# MySQL Images

## Version

### 5.7
```
$ docker build -t=nethost/mysql:5.7-debian .
$ docker push nethost/mysql:5.7-debian
$ docker pull nethost/mysql:5.7-debian
```

### 5.6
```
$ docker build -t=nethost/mysql:5.6-debian .
$ docker push nethost/mysql:5.6-debian
$ docker pull nethost/mysql:5.6-debian
```

### 5.5
```
$ docker build -t=nethost/mysql:5.5-debian .
$ docker push nethost/mysql:5.5-debian
$ docker pull nethost/mysql:5.5-debian
```

## How to use this image ?

### Start a mysql server instance

```
$ docker run --name some-mysql -p 3309:3306 -e MYSQL_ROOT_PASSWORD=1014 -d nethost/mysql:5.7-debian
```
where some-mysql is the name you want to assign to your container, my-secret-pw is the password to be set for the MySQL root user and tag is the tag specifying the MySQL version you want. See the list above for relevant tags.


