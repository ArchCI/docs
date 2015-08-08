### worker用法

---

本地运行simple-worker。

```
root@archci:~/go/src/github.com/ArchCI/simple-worker# go run worker.go
Start ArchCI simple worker
test-project

Success to clone the code
Docker image: "golang:1.4"
Success to create archci.sh

Success to run docker run --rm -v $PWD/test-project:/project golang:1.4 /project/archci.sh > docker.log 2>&1 ; echo $? > exit_code.log

Success to delete the code
Sleep 60 seconds for next task
^Cexit status 2
```

然后检查测试结果和日志。

```
root@archci:~/go/src/github.com/ArchCI/simple-worker# cat exit_code.log
0
root@archci:~/go/src/github.com/ArchCI/simple-worker# cat docker.log
ok      command-line-arguments  0.002s
```
