# docker-compose up 

## 使用方法
` docker-compose [参数] up [服务名称]`

## 参数
* `-d` 后台运行（守护进程模式）
* `-f` 指定非默认的 compose 文件（如 docker-compose.prod.yml）
* `--build` 启动前重新构建镜像（适合代码更新后）
* `-scale` 扩展容器数量（如 -scale web=3 表示启动 3 个 web 容器）

## 实例
```
# 前台启动 compose 应用（按 Ctrl+C 停止）
docker-compose up

# 后台启动 compose 应用
docker-compose up -d

# 指定自定义 compose 文件启动
docker-compose -f docker-compose.prod.yml up -d

# 启动前重新构建镜像
docker-compose up -d --build

# 只启动 compose 中的 web 服务
docker-compose up -d web

# 扩展 web 服务到 3 个容器
docker-compose up -d --scale web=3
```