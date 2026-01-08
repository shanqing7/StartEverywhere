# docker image 
## 使用方法
`docker images [参数] [镜像名称]`

## 参数
* `-a` 列出所有镜像（包括中间层镜像，默认隐藏）
* `-q` 只输出镜像 ID
* `--filter` 过滤镜像（如过滤虚悬镜像：dangling=true）

## 实例
```
# 查看所有本地镜像
docker images

# 只查看 ubuntu 相关镜像
docker images ubuntu

# 只输出所有镜像的 ID
docker images -q

# 过滤出虚悬镜像（无标签的镜像，标记为 <none>）
docker images --filter "dangling=true"
```

