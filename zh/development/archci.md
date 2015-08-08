### archci详解

---

### 简介

archci是ArchCI项目的Web服务器和UI，他负责接受客户端的请求、收集worker的测试结果、并且展示到Web界面中。

### 启动服务

```
docker run -d --net=host archci/archci
```

### 参与开发

archci使用golang开发，依赖[beego](https://github.com/astaxie/beego)框架，参与archci开发需要配置好$GOPATH。

archci项目包含了所有稳定的依赖库，可以通过`godep go build`直接编译。

当然你可以clone源码，通过`go get`下载依赖库，然后`go build`编译。

