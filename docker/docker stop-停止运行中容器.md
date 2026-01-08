# docker stop

## 使用方法
`docker stop [参数] 容器名称/ID [容器名称/ID ...] `

## 参数
* `-t` 停止超时时间（默认 10 秒，如 -t 5 表示 5 秒后强制停止）

## 实例
```
# 停止单个容器
docker stop my-nginx

# 停止多个容器（用空格分隔）
docker stop my-ubuntu my-mysql

# 5 秒后强制停止容器
docker stop -t 5 my-nginx

# 停止所有运行中的容器（结合 docker ps -q）
docker stop $(docker ps -q)
```