### 安装指南

---

通过docker容器运行。

```
docker run -d -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 mysql:5.7
docker run -d -p 6379:6379 redis
docker run -d --net=host archci/archci
docker run -d --net=host --privileged archci/simple-worker
```


