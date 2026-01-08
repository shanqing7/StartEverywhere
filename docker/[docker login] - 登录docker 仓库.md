# docker login

## 使用方法
`docker login [参数] [仓库地址]`

## 参数
* `-u` 指定用户名
* `-p` 	指定密码（不推荐明文，省略会交互式输入）
* `--password-stdin` 从标准输入读取密码（安全，适合脚本）

## 实例
```
# 登录 Docker Hub（交互式输入用户名/密码）
docker login

# 登录 Docker Hub（指定用户名，交互式输密码）
docker login -u my-username

# 登录私有仓库（如 192.168.1.100:5000）
docker login 192.168.1.100:5000

# 脚本中安全登录（从文件读取密码）
cat password.txt | docker login -u my-username --password-stdin
```