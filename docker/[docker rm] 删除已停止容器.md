# docker rm

## 使用方法
`docker rm [参数] 容器名称/ID [容器名称/ID ...] `

## 参数
* `-f` 强制删除运行中的容器（不推荐，优先 stop 再 rm）
* `-v` 删除容器关联的数据卷（避免卷残留）
## 实例
```
# 删除单个已停止的容器
docker rm my-ubuntu

# 删除多个容器
docker rm my-ubuntu my-mysql

# 强制删除运行中的容器（慎用）
docker rm -f my-nginx

# 删除容器并清理关联的数据卷
docker rm -v my-mysql

# 删除所有已停止的容器
docker rm $(docker ps -aq --filter "status=exited")
```