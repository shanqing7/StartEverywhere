# docker inspect

## 使用方法
`docker inspect [参数] 容器/镜像/网络/卷名称/ID`

## 参数
* `-f` 过滤输出（使用 Go 模板提取指定字段）
* `-s`  显示镜像的大小（仅对镜像生效）

## 实例
```
# 查看容器的所有详细信息（JSON 格式）
docker inspect my-nginx

# 只提取容器的 IP 地址
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' my-nginx

# 只提取镜像的创建时间
docker inspect -f '{{.Created}}' ubuntu:20.04

# 查看镜像的大小
docker inspect -s ubuntu:20.04
```

## 示例
```json
heria@HS-20241227QHMS:~/wyl_stu/docker$ docker inspect ae378fb1959c
[
    {
        "Id": "ae378fb1959c454854762329e96f88941c457d993efdd9a593cf19de7428197a",
        "Created": "2025-12-02T08:11:29.087695922Z",
        "Path": "/bin/bash",
        "Args": [],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 11393,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2026-01-05T11:17:25.719115682Z",
            "FinishedAt": "2026-01-04T02:37:14.192462303Z"
        },
        "Image": "sha256:9b9cb95443b5f846cd3c8cfa3f64e63b6ba68de2618a08875a119c81a8f96698",
        "ResolvConfPath": "/var/lib/docker/containers/ae378fb1959c454854762329e96f88941c457d993efdd9a593cf19de7428197a/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/ae378fb1959c454854762329e96f88941c457d993efdd9a593cf19de7428197a/hostname",
        "HostsPath": "/var/lib/docker/containers/ae378fb1959c454854762329e96f88941c457d993efdd9a593cf19de7428197a/hosts", 
        "LogPath": "/var/lib/docker/containers/ae378fb1959c454854762329e96f88941c457d993efdd9a593cf19de7428197a/ae378fb1959c454854762329e96f88941c457d993efdd9a593cf19de7428197a-json.log",
        "Name": "/test_ubuntu",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "bridge",
            "PortBindings": {},
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "ConsoleSize": [
                42,
                163
            ],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "host",
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": [],
            "BlkioDeviceWriteBps": [],
            "BlkioDeviceReadIOps": [],
            "BlkioDeviceWriteIOps": [],
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": null,
            "Ulimits": [],
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/interrupts",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware",
                "/sys/devices/virtual/powercap"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "ID": "ae378fb1959c454854762329e96f88941c457d993efdd9a593cf19de7428197a",
                "LowerDir": "/var/lib/docker/overlay2/762a66016c452c7408545f8a8128822d71a05b78d244c67e9e1c060a38ffc030-init/diff:/var/lib/docker/overlay2/ee6c76b51fdc9fe1045f2bc951f1033e9ccf0e885b2ab659d78be4912608a591/diff:/var/lib/docker/overlay2/e14b78206cf23b3726df127964291547ccf4ae79a6cc6a673aec23e9526736cb/diff:/var/lib/docker/overlay2/458a47ce3d404b48efedfba7c31cf28ad6b0f775a29ffdc6c97faccd8a5abda1/diff:/var/lib/docker/overlay2/5e6eb6f1009f5028ab2563fc7eb37c730a856f48c8a2726c7049dcd65a258483/diff",
                "MergedDir": "/var/lib/docker/overlay2/762a66016c452c7408545f8a8128822d71a05b78d244c67e9e1c060a38ffc030/merged",
                "UpperDir": "/var/lib/docker/overlay2/762a66016c452c7408545f8a8128822d71a05b78d244c67e9e1c060a38ffc030/diff",
                "WorkDir": "/var/lib/docker/overlay2/762a66016c452c7408545f8a8128822d71a05b78d244c67e9e1c060a38ffc030/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "ae378fb1959c",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": true,
            "OpenStdin": true,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
            ],
            "Cmd": [
                "/bin/bash"
            ],
            "Image": "ubuntu:15.10",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": {}
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "0d67d115eaf6bf8ed836ac53b0a3851242a813a7ca818a13779813d5689ba87a",
            "SandboxKey": "/var/run/docker/netns/0d67d115eaf6",
            "Ports": {},
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "0355bac6f225efb193391077bc1fe836b98aab5e38b1d230cb196a01498c4566",
            "Gateway": "172.17.0.1",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "172.17.0.2",
            "IPPrefixLen": 16,
            "IPv6Gateway": "",
            "MacAddress": "7e:69:c6:63:2e:29",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "MacAddress": "7e:69:c6:63:2e:29",
                    "DriverOpts": null,
                    "GwPriority": 0,
                    "NetworkID": "c3c3c4ec9e96fbc57cb448649707273926f08608e044862c0fced4c08093d946",
                    "EndpointID": "0355bac6f225efb193391077bc1fe836b98aab5e38b1d230cb196a01498c4566",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.2",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "DNSNames": null
                }
            }
        }
    }
]
```