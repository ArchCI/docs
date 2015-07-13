### 启动archci

---

### 简介

archci是ArchCI项目的Web服务器和UI，他负责接受客户端的请求、收集worker的测试结果、并且展示到Web界面中。

目前archci基于开源的React框架开发，前端使用Bootstrap、npm等工具管理。


### 搭建开发环境

```
git clone https://github.com/ArchCI/archci.git
cd archci/static/
npm install
npm run build
cd ../
go get
go build
./archci
```

### 环境依赖

* golang
* nodejs
* npm

如果出现错误`This failure might be due to the use of legacy binary "node"`，请安装`nodejs-legacy`。