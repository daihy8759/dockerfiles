# create debian-ssh

- build image

```sh
docker build -t debian-ssh:latest .
```

- run

```sh
docker run -d -p 2000:22 debian-ssh
```

- 删除开启ssh的docker容器信息

```sh
ssh-keygen -R "[127.0.0.1]:2000"
```

- 连接

```sh
ssh -p2000 root@127.0.0.1
```
