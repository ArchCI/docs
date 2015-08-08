### aci用法

---

编译运行`aci`非常简单，使用前确保`golang`已经安装好。

```
➜  aci git:(master) go build
➜  aci git:(master) ./aci
NAME:
   aci - command-line client for ArchCI

USAGE:
   aci [global options] command [command options] [arguments...]

VERSION:
   0.1

COMMANDS:
   create_account       create the new account
   help, h              Shows a list of commands or help for one command

GLOBAL OPTIONS:
   -t, --token          server auth token [$ARCHCI_TOKEN]
   -s, --server         server address [$ARCHCI_SERVER]
   --help, -h           show help
   --version, -v        print the version
```