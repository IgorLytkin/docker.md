liv@singularity:~$ hostnamectl
 Static hostname: singularity
       Icon name: computer-vm
         Chassis: vm
      Machine ID: c3f3c2a325254275b58ddc82c9068b5c
         Boot ID: d12220948d0540a78e3b43fe8fe70c81
  Virtualization: kvm
Operating System: Ubuntu 22.04.4 LTS
          Kernel: Linux 5.15.0-100-generic
    Architecture: x86-64
 Hardware Vendor: QEMU
  Hardware Model: Standard PC _i440FX + PIIX, 1996_
  
На VPS singularity:
liv@singularity:~$ docker -v
Docker version 25.0.3, build 4debf41

liv@singularity:~$ docker version
Client: Docker Engine - Community
 Version:           25.0.3
 API version:       1.44
 Go version:        go1.21.6
 Git commit:        4debf41
 Built:             Tue Feb  6 21:13:09 2024
 OS/Arch:           linux/amd64
 Context:           default

Server: Docker Engine - Community
 Engine:
  Version:          25.0.3
  API version:      1.44 (minimum version 1.24)
  Go version:       go1.21.6
  Git commit:       f417435
  Built:            Tue Feb  6 21:13:09 2024
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.28
  GitCommit:        ae07eda36dd25f8a1b98dfbf587313b99c0190bb
 runc:
  Version:          1.1.12
  GitCommit:        v1.1.12-0-g51d5e94
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0

Первые шаги

liv@singularity:~$ docker run debian echo "Hello World"
Unable to find image 'debian:latest' locally
latest: Pulling from library/debian
7bb465c29149: Pull complete
Digest: sha256:4482958b4461ff7d9fabc24b3a9ab1e9a2c85ece07b2db1840c7cbc01d053e90
Status: Downloaded newer image for debian:latest
Hello World
liv@singularity:~$ docker run debian echo "Hello World"
Hello World

**08.03.2024**

liv@singularity:~$ uname -a
Linux singularity **5.15.0-100-generic** #110-Ubuntu SMP Wed Feb 7 13:27:48 UTC 2024 x86_64 x86_64 x86_64 GNU/Linux

liv@singularity:~$ docker --version
Docker version 25.0.4, build 1a576c5

liv@singularity:~$ docker compose version
Docker Compose version v2.24.7

 liv@singularity:~$ docker volume ls
DRIVER    VOLUME NAME
local     2d75839793e0a63e189f1a0e63eb952fdfde1ced5d6326b84dd6ee9a335d2252
local     2e59006af1c287f1f0abcdfe384d72077128fdb0d9f6d7b46fe85db25003e26b
local     5af367f9648c5721989790a6f9c07760ae584534c3139b895c27650e5083cf9e
local     0538bf76a11f0ced90b4d8685fd7e6b9f8a20f1f18afbb1ff99dbaedb898dc7a
local     a8a4aa2154b1be7fb4e8891507ffe5fc30d47547ccbe3cce036a0b0f2462679a
local     fsmbot_fsmdata
local     fsmbot_pgdata
local     portainer_data

![[Pasted image 20240309081136.png]]

liv@singularity:~$ docker inspect -f {{.Mounts}} fsmbot-redis-1
[{volume 0538bf76a11f0ced90b4d8685fd7e6b9f8a20f1f18afbb1ff99dbaedb898dc7a /var/lib/docker/volumes/0538bf76a11f0ced90b4d8685fd7e6b9f8a20f1f18afbb1ff99dbaedb898dc7a/_data **/data** local  true }]

/data в контейнере = /var/lib/docker/volumes/0538bf76a11f0ced90b4d8685fd7e6b9f8a20f1f18afbb1ff99dbaedb898dc7a/data на VPS.


liv@singularity:~$ **docker info**
Client: Docker Engine - Community
 Version:    25.0.4
 Context:    default
 Debug Mode: false
 Plugins:
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.13.0
    Path:     /usr/libexec/docker/cli-plugins/docker-buildx
  compose: Docker Compose (Docker Inc.)
    Version:  v2.24.7
    Path:     /usr/libexec/docker/cli-plugins/docker-compose

Server:
 Containers: 14
  Running: 6
  Paused: 0
  Stopped: 8
 Images: 24
 Server Version: 25.0.4
 Storage Driver: overlay2
  Backing Filesystem: extfs
  Supports d_type: true
  Using metacopy: false
  Native Overlay Diff: true
  userxattr: false
 Logging Driver: json-file
 Cgroup Driver: systemd
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 Swarm: inactive
 Runtimes: io.containerd.runc.v2 runc
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: ae07eda36dd25f8a1b98dfbf587313b99c0190bb
 runc version: v1.1.12-0-g51d5e94
 init version: de40ad0
 Security Options:
  apparmor
  seccomp
   Profile: builtin
  cgroupns
 Kernel Version: 5.15.0-100-generic
 Operating System: Ubuntu 22.04.4 LTS
 OSType: linux
 Architecture: x86_64
 CPUs: 2
 Total Memory: 3.819GiB
 Name: singularity
 ID: dfb69f4f-67fc-4153-96e5-f1e3a4b33722
 Docker Root Dir: /var/lib/docker
 Debug Mode: false
 Username: igorlytkin
 Experimental: false
 Insecure Registries:
  127.0.0.0/8
 Live Restore Enabled: false
