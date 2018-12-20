Redis cluster test
===================

## Redis Cluster
* https://redis.io/topics/cluster-tutorial
* https://www.digitalocean.com/community/tutorials/how-to-install-secure-redis-centos-7
* https://redis.io/topics/security

## Redis client

### Create Cluster
```bash
$ docker run -it --net=host redis redis-cli \
    --cluster create 127.0.0.1:7000 127.0.0.1:7001 \
    127.0.0.1:7002 127.0.0.1:7003 127.0.0.1:7004 127.0.0.1:7005 \
    --cluster-replicas 1
```

### Info
```bash
$ docker run -it --net=host redis redis-cli -p 7000 info
```