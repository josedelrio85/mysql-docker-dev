# MySQL Development 

* Run a MySQL docker image to deploy a local development MySQL instance.


## How to run the project

```bash
docker-compose up -d
```

## How to connect to the instance

```bash
mysql -hlocalhost -u[user] -p[password] -P[port] --protocol=tcp
```


## How to connect to the instance [hard method]

```bash
docker network inspect mysql-docker-development_mysql-development
```

* Get the IP port and use it to connect to the instance

```bash
mysql -h172.21.0.2 -uroot_bsc -proot_bsc
```