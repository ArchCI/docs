### 项目简介

---

### 持续集成

ArchCI是开源的CI系统，他为公司内部或开源项目提供持续集成服务，项目只需添加.archci.yml文件，有新代码提交时会自动触发测试，由worker执行测试并将结果返回给archci前端展示。

* 与Jenkins类似，都可以提供公司内部以及开源项目的持续集成服务，但ArchCI使用了更轻量化的Docker容器。
* 与TravisCI类似，都只需在你的项目添加Yaml文件即可执行测试，但ArchCI使用Golang实现更易于部署。
* 与Drone类似，都是基于Docker、Golang实现并且提供API和客户端工具，但ArchCI是100%开源有更多特性。

### 组件介绍

archci是整个项目API服务器和前端展示页面，负责接受客户端的请求，并且收集worker的测试报告，最后展示给用户。

worker是真正负责执行测试的组件，他会调用底层的docker容器执行测试脚本，最后将结果返回给archci服务器，如果测试项目过多可以通过多运行几个worker来分摊压力。

目前ArchCI服务需要archci和一个或以上worker即可，所有组件都是通过go实现的，可以直接下载二进制文件在本地运行。

