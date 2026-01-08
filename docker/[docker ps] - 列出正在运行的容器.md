# docker ps 命令
## 使用方法
`docker ps [参数]`

## 参数
* `-a` 列出所有容器（运行中 + 已停止）
* `-q` 只输出容器 ID（常用于批量操作）
* `--format` 自定义输出格式（如只看名称和状态）

## 实例
```
# 查看正在运行的容器（默认）
docker ps

# 查看所有容器（包括已停止）
docker ps -a

# 只输出所有容器的 ID
docker ps -aq

# 自定义输出：容器ID、名称、状态
docker ps --format "table {{.ID}}\t{{.Names}}\t{{.Status}}"
```
