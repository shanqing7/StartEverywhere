# docker version

## 使用方法
`docker version [参数] `

## 参数
* `-f` 过滤输出（如只看客户端版本
* `--format json` 以 JSON 格式输出

## 实例
```
# 查看完整版本信息
docker version

# 只查看客户端版本
docker version -f '{{.Client.Version}}'

# 以 JSON 格式输出所有版本信息
docker version --format json

```