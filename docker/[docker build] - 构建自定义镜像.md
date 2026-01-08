# docker build

## 使用方法

`docker build [参数] 构建上下文路径（通常是 . 表示当前目录）`

## 参数
* `-t` 给镜像打标签（格式：名称：版本，如 my-app:1.0）
* `-f` 指定非默认名称的 Dockerfile（如 Dockerfile.prod）
* `--no-cache` 不使用缓存构建（强制重新编译所有步骤）

## 实例
```
# 基于当前目录的 Dockerfile 构建，标签为 my-image:v1
docker build -t my-image:v1 .

# 指定自定义 Dockerfile（如 Dockerfile.dev）构建
docker build -t my-image:dev -f Dockerfile.dev .

# 不使用缓存构建（适合依赖更新后）
docker build --no-cache -t my-image:v2 .
```
`