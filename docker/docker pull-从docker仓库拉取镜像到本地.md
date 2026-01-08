# docker pull
## 使用方法
`docker pull [参数] 镜像名称[:标签]`

## 参数
* `--platform` 指定平台（如 arm64、amd64，跨架构拉取）
* `-a` 拉取该镜像的所有标签版本

## 实例
```
# 拉取 ubuntu 最新版本镜像
docker pull ubuntu

# 拉取指定版本的 ubuntu（20.04）
docker pull ubuntu:20.04

# 拉取阿里云镜像仓库的 Nginx（私有仓库需先登录）
docker pull registry.cn-hangzhou.aliyuncs.com/library/nginx:1.24

# 跨架构拉取（如 arm64 架构的 ubuntu）
docker pull --platform linux/arm64 ubuntu:22.04

```
