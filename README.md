# MySQL Development

* Run a MySQL docker image to deploy a local development MySQL instance.


## How to run the project

```bash
docker-compose up -d
```

## How to connect to the instance

```bash
docker network inspect mysql-docker-development_mysql-development
```

* Get 
mysql -h172.21.0.2 -uroot_bsc -proot_bsc
```



docker inspect -f '{{range.Containers}}{{.IPv4Address}}{{end}}' mysql-docker-development_mysql-development
172.21.0.2/16

// TODO remove 3 last characters

CID=$(docker inspect -f '{{range.Containers}}{{.IPv4Address}}{{end}}' mysql-docker-development_mysql-development) && mysql -h$CID -uroot_bsc -proot_bsc

CID=$(docker inspect -f '{{range.Containers}}{{.IPv4Address}}{{end}}' mysql-docker-development_mysql-development) && mysql -h$CID -uroot_bsc -proot_bsc


docker inspect mysql-docker-development_mysql-development | grep "IPAddress"
"IPv4Address": "172.21.0.2/16",