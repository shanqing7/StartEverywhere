# docker stats

## 使用方法
`docker stats [参数] [容器名称/ID]`

## 参数
* `-a` 显示所有容器（包括已停止的，默认只显示运行中）
* `--no-stream` 只输出一次统计信息（非实时）
* `--format` 自定义输出格式
## 实例
```
# 实时查看所有运行中容器的资源使用
docker stats

# 只查看指定容器的资源使用
docker stats my-nginx my-mysql

# 只输出一次统计信息（非实时）
docker stats --no-stream

# 自定义输出：容器名称、CPU 使用率、内存使用率
docker stats --format "table {{.Name}}\t{{.CPUPerc}}\t{{.MemPerc}}"
```
