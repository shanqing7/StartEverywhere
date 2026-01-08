# docker restart

## 使用方法
` docker restart [参数] 容器名称/ID [容器名称/ID ...]`

## 参数
* `-t` 	停止超时时间（默认 10 秒）

## 实例
```
# 重启单个容器
docker restart my-nginx

# 重启多个容器
docker restart my-nginx my-mysql

# 5 秒超时后重启容器
docker restart -t 5 my-nginx
```