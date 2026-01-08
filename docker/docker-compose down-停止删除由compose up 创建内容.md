# docker-compose down

## 使用方法
`docker-compose [参数] down`

## 参数
* `-v` 删除 compose 创建的数据卷（谨慎，会丢失持久化数据）
* `-rmi` 删除 compose 构建的镜像（如 --rmi all 表示删除所有相关镜像）
* `--remove-orphans` 删除 compose 文件中未定义的容器
## 实例
```
# 停止并删除容器、网络（保留卷和镜像）
docker-compose down

# 停止并删除容器、网络、数据卷（慎用，数据丢失）
docker-compose down -v

# 停止并删除容器、网络，同时删除构建的镜像
docker-compose down --rmi all

# 删除 compose 文件中未定义的容器
docker-compose down --remove-orphans
```