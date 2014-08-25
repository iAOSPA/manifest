# iAOSPA #

## 同步源码 ##

[Repo](http://source.android.com/source/developing.html) 是一个由 Google 提供的工具，它简化了在同步Android源码时使用 [Git](http://git-scm.com/book) 的工作.

### 安装 Repo ###

```bash
# 创建一个存放 Repo 的目录并将这个目录添加到PATH里
$ mkdir ~/bin
$ PATH=~/bin:$PATH

# 下载 Repo 启动器
$ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo

# 让 Repo 可执行
$ chmod a+x ~/bin/repo
```

### 初始化 Repo ###

```bash
# 创建一个目录来存放源码
# 它可以放在任何地方 (但必须是大小写敏感的文件系统)
$ mkdir WORKSPACE
$ cd WORKSPACE

# 在创建好的目录里安装repo
# 如果你想提交 PATCH，请用真实的邮件和用户名
$ repo init -u https://github.com/iAOSPA/manifest -b n5x
```

### 下载源码 ###

```bash
# 让 Repo 为你做完所有事情
$ repo sync
```

## 编译 ##

编译器工具脚本 `./rom-build.sh` 可以自动为特定的device进行所有的编译步骤. 要获取 device 值，你只需要填入device的代号(例如,
Nexus 5 的codename为'hammerhead').

```bash
# 前往源码文件夹的根目录...
$ cd WORKSPACE
# ...然后运行编译器工具脚本.
$ ./rom-build.sh DEVICE
```
