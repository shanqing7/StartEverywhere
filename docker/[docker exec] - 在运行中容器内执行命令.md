# docker exec

## 使用方法
`docker exec [参数] 容器名称/ID 要执行的命令`

## 参数
* `-it` 交互式执行（进入容器终端）
* `-d` 后台执行命令（不进入终端）
* `-u` 指定执行命令的用户（如 root）

## 实例
```
# 进入运行中的 my-ubuntu 容器，打开 bash 终端
docker exec -it my-ubuntu bash

# 进入容器并指定用户（root）
docker exec -it -u root my-ubuntu bash

# 后台执行命令：在容器内创建 /tmp/test.txt 文件
docker exec -d my-ubuntu touch /tmp/test.txt

# 查看容器内的 nginx 配置文件
docker exec -it my-nginx cat /etc/nginx/nginx.conf
```
