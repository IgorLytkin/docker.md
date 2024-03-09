
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

