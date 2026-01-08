# docker logs

## 使用方法
`docker logs [参数] 容器名称/ID`
## 参数
* `-f` 实时跟踪日志（类似 tail -f）
* `-t` 显示日志时间戳
* `--tail` 只显示最后 N 行日志（如 --tail 100）
* `--since` 	显示指定时间后的日志（如 --since 2026-01-01 或 --since 1h）

## 实例
```
# 查看容器所有日志
docker logs my-nginx

# 实时跟踪日志（实时查看新增日志）
docker logs -f my-nginx

# 显示最后 50 行日志，并带时间戳
docker logs -t --tail 50 my-nginx

# 查看近 1 小时的日志
docker logs --since 1h my-nginx

# 查看 2026-01-01 之后的日志
docker logs --since 2026-01-01 my-nginx
```