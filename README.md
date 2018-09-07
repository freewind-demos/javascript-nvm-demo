JavaScript Nvm Demo
===================

[nvm](https://github.com/creationix/nvm) 是一个用来管理node版本的shell工具，可以让我们方便的显示、下载、启用某个版本的node.

安装方法在其主页上有，需要注意的是，如果使用的是fish，需要使用[fisherman/fish](https://github.com/fisherman/nvm)插件。

常用功能：

- `nvm --version`：显示nvm版本号，检查是否能正常运行
- `nvm ls-remote`：显示可供安装的node版本
- `nvm ls-remote --lts`：只显示可供安装的长期支持的node版本
- `nvm ls`：显示本地已经安装的版本
- `nvm install v10.10.0`：安装指定版本的node
- `nvm use 8`：使用`v8.x.x`中的最新版本
- `nvm current`：显示当前正在使用的node版本
- `nvm use`：如果当前目录下有`.nvmrc`文件，则使用其中指定的版本号

注意：

在nvm中，不支持自动根据目录下`.nvmrc`切换版本，必须手动执行`nvm use`

切换版本
----

```
$ cd project1

$ nvm use
Found '/Users/freewind/workspace/javascript-nvm-demo/project1/.nvmrc' with version <v8.11.2>
Now using node v8.11.2 (npm v5.6.0)

$ node -v
v8.11.2
```

```
$ cd project2

$ nvm use
Found '/Users/freewind/workspace/javascript-nvm-demo/project2/.nvmrc' with version <v10.10.0>
Now using node v10.10.0 (npm v6.4.1)

$ node -v
v10.10.0
```