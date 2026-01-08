# 网络映射

## 指定容器绑定 主机端口
`docker run -d -p 127.0.0.1:5001:5000 flask-webapp python app.py`

## 容器创建
### python 程序，端口打印
```python
"app.py"
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return "Hello World!"

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
```
### Dockerfile
```
heria@HS-20241227QHMS:~/wyl_stu/docker/flask-demo$ cat Dockerfile 
# 使用新版 Python 3.11 轻量镜像（无格式警告）
FROM python:3.11-slim

# 设置工作目录
WORKDIR /app

# 复制应用代码到容器
COPY app.py .

# 安装 Flask（用清华源加速，避免下载慢）
RUN pip install flask -i https://pypi.tuna.tsinghua.edu.cn/simple

# 声明容器暴露 5000 端口（规范写法）
EXPOSE 5000

# 启动 Flask 应用
CMD ["python", "app.py"]
```
### 打包镜像
`docker build -t flask-webapp .`

### 示例
![4fa8bbed067058e018e4562444426d0f.png](../../_resources/4fa8bbed067058e018e4562444426d0f.png)
