# docker rmi 
## 使用方法
`docker rmi [参数] 镜像名称/ID [镜像名称/ID ...] `

## 参数
* `-f` 强制删除镜像（即使被容器引用，需谨慎）
* `--no-prune` 不删除镜像的中间层（默认会删除）

## 实例
```
# 删除单个镜像（按标签）
docker rmi my-image:v1

# 删除多个镜像（按 ID）
docker rmi 123456 abcdef

# 强制删除被容器引用的镜像（会导致依赖容器无法启动）
docker rmi -f my-image:v1

# 删除所有虚悬镜像（<none> 标签）
docker rmi $(docker images --filter "dangling=true" -q)
```
