### 启动Worker

---

### 简介

Worker是ArchCI项目中执行测试的组件，他可以随着测试项目的增加而水平拓展，目前支持simple-worker和kubernette-worker。

### Simple-workder

Simple-worker是最简单的worker实现，支持Linux、Windows、MacOS等平台的二进制文件，他以来底层的docker来执行测试任务。

### 搭建开发环境

```
git clone https://github.com/ArchCI/simple-worker.git
cd simple-worker/
go get
go build
./simple-worker
```