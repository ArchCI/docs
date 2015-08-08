### worker详解

---

### 简介

Worker是ArchCI项目中执行测试的组件，他可以随着测试项目的增加而水平拓展，目前支持simple-worker和kubernette-worker。

### Simple-workder

Simple-worker是最简单的worker实现，支持Linux、Windows、MacOS等平台的二进制文件，他以来底层的docker来执行测试任务。

### 参与开发

由于ArchCI基于docker容器进行持续集成测试，因此部署worker前需确保本地docker环境已经启动，Mac或者Windows用户在boot2docker环境下也可以安装测试。

Simple-worker的所有依赖包已经在Godeps目录下，通过`godep go build`即可编译，也可以通过`go get`和`go build`在本地编译运行。

编译后生成二进制文件`worker`，直接运行即可，目前运行simple-worker前需要启动mysql和redis服务。
