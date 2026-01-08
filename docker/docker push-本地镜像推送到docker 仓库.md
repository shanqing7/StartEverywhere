# docker push 

## 命令
```
docker push [参数] 镜像名称[:标签]
```

## 参数
* `--disable-content-trust` 禁用镜像签名验证（加速推送）

## 实例
```
# 推送镜像到 Docker Hub（需先 docker login，镜像标签需包含用户名，如 username/my-image:v1）
docker tag my-image:v1 username/my-image:v1  # 先打标签（必须包含用户名）
docker push username/my-image:v1

# 推送镜像到私有仓库（如本地仓库 192.168.1.100:5000）
docker tag my-image:v1 192.168.1.100:5000/my-image:v1
docker push 192.168.1.100:5000/my-image:v1
```
