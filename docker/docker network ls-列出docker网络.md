# docker network ls

## 使用方法
`docker network ls [参数]`

## 参数
* `-q` 只输出网络 ID
* `--filter` 过滤网络（如类型：type=bridge）

## 实例
```
# 查看所有 Docker 网络
docker network ls

# 只输出网络 ID
docker network ls -q

# 过滤出桥接模式（bridge）的网络
docker network ls --filter "type=bridge"
```

## 示例
![68e00af01999190c78d2e93ab780bd0a.png](../_resources/68e00af01999190c78d2e93ab780bd0a-2.png)