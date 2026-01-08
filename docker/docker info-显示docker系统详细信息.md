# docker info 

## 使用方法
`docker info [参数] `

## 参数
* `-f` 过滤输出（提取指定字段）

## 实例
```
# 查看所有 Docker 系统信息
docker info

# 只提取 Docker 存储驱动
docker info -f '{{.Driver}}'

# 只提取运行中的容器数
docker info -f '{{.ContainersRunning}}'
```

## 示例
```
Client: Docker Engine - Community
 Version:    28.5.1
 Context:    default
 Debug Mode: false
 Plugins:
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.29.1
    Path:     /usr/libexec/docker/cli-plugins/docker-buildx
  compose: Docker Compose (Docker Inc.)
    Version:  v2.40.0
    Path:     /usr/libexec/docker/cli-plugins/docker-compose
  model: Docker Model Runner (Docker Inc.)
    Version:  v0.1.44
    Path:     /usr/libexec/docker/cli-plugins/docker-model

Server:
 Containers: 15
  Running: 1
  Paused: 0
  Stopped: 14
 Images: 2
 Server Version: 28.5.1
 Storage Driver: overlay2
  Backing Filesystem: extfs
  Supports d_type: true
  Using metacopy: false
  Native Overlay Diff: true
  userxattr: false
 Logging Driver: json-file
 Cgroup Driver: cgroupfs
 Cgroup Version: 1
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 CDI spec directories:
  /etc/cdi
  /var/run/cdi
 Swarm: inactive
 Runtimes: runc io.containerd.runc.v2
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: b98a3aace656320842a23f4a392a33f46af97866
 runc version: v1.3.0-0-g4ca628d1
 init version: de40ad0
 Security Options:
  seccomp
   Profile: builtin
 Kernel Version: 5.10.16.3-microsoft-standard-WSL2
 Operating System: Ubuntu 22.04.1 LTS
 OSType: linux
 Architecture: x86_64
 CPUs: 16
 Total Memory: 7.634GiB
 Name: HS-20241227QHMS
 ID: 0185221c-44b3-4d60-9849-1a2b35730eae
 Docker Root Dir: /var/lib/docker
 Debug Mode: false
 Experimental: false
 Insecure Registries:
  ::1/128
  127.0.0.0/8
 Live Restore Enabled: false

WARNING: No blkio throttle.read_bps_device support
WARNING: No blkio throttle.write_bps_device support
WARNING: No blkio throttle.read_iops_device support
WARNING: No blkio throttle.write_iops_device suppor
```