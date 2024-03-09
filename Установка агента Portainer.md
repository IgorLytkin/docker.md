docker run -d \ -p 9001:9001 \ --name portainer_agent \ --restart=always \ -v /var/run/docker.sock:/var/run/docker.sock \ -v /var/lib/docker/volumes:/var/lib/docker/volumes \ portainer/agent:2.16.2

liv@singularity:~$ docker run -d \
  -p 9001:9001 \
  --name portainer_agent \
  --restart=always \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v /var/lib/docker/volumes:/var/lib/docker/volumes \
  portainer/agent:2.16.2
Unable to find image 'portainer/agent:2.16.2' locally
2.16.2: Pulling from portainer/agent
772227786281: Pull complete
96fd13befc87: Pull complete
7cc53cdd8cd9: Pull complete
dd9ba6ee194f: Pull complete
f8f397f74925: Pull complete
7d7656593111: Pull complete
Digest: sha256:2c1abfac4937923e625be5f63a15f49a19cc4cca247c50f8746a9222023865a3
Status: Downloaded newer image for portainer/agent:2.16.2
64f23757b218216c024c91e6b97a14ace2016ea210731e5be76d5b6cd318041a

Соединение Portianer на ноутбуке Dell с агентом Portainer на VPS Singularity

