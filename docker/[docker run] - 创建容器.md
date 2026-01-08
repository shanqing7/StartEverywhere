# docker run 命令

## 使用方法

`docker run [参数] 镜像名称[:标签] [容器内执行的命令]`

## 参数

- `-d` 后台运行容器（守护进程模式）
- `-it` 交互式终端（可输入命令）
- `-P` 端口映射（宿主端口：容器端口）
- `-v` 数据卷挂载（宿主路径：容器路径）
- `--name` 自定义容器名称（默认随机名称）
- `-e` 设置环境变量

## 实例

```bash
# 后台运行 ubuntu 容器，默认执行 bash（无前台进程会立即退出）
docker run -d ubuntu

# 交互式运行 ubuntu，进入容器终端
docker run -it --name my-ubuntu ubuntu /bin/bash

# 运行 Nginx，映射宿主 8080 端口到容器 80 端口，后台运行
docker run -d --name my-nginx -p 8080:80 nginx

# 运行 MySQL，设置密码，挂载数据卷到宿主 /data/mysql
docker run -d --name my-mysql -e MYSQL_ROOT_PASSWORD=123456 -v /data/mysql:/var/lib/mysql mysql:8.0
```