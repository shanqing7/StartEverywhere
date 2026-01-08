# docker start

## 使用方法
`docker start [参数] 容器名称/ID [容器名称/ID ...]`

## 参数
* `-i` 以交互式启动（配合 -a 输出日志）
* `-a` 附加到容器的标准输入 / 输出（查看启动日志）

## 实例
```
# 启动单个已停止的容器
docker start my-nginx

# 启动多个容器
docker start my-ubuntu my-mysql

# 启动容器并查看启动日志（附加输出）
docker start -a my-nginx

# 启动所有已停止的容器
docker start $(docker ps -aq --filter "status=exited")
```