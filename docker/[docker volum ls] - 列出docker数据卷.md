# docker volums ls

## 使用方法 
`docker volume ls [参数]`

## 参数
* `-q` 只输出卷 ID
* `--filter` 过滤卷（如名称包含 mysql：name=mysql）

## 实例
```
# 查看所有数据卷
docker volume ls

# 只输出卷 ID
docker volume ls -q

# 过滤出名称包含 mysql 的卷
docker volume ls --filter "name=mysql"
```