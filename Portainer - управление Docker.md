https://academy.portainer.io/install/#/

"Узел" можно просто описать как "сервер" (будь то реальный физический сервер, виртуальная машина, Raspberry Pi, ваш настольный компьютер или ноутбук, промышленный компьютер или встроенное вычислительное устройство), который способен запускать контейнеры (через Docker, Kubernetes или другой orchestrator), который либо запускает сервер Portainer, либо находится под управлением установленного сервера Portainer.

DEV - development, разработка
UAT - User Accaptance Testing

Стенд для нагрузочного тестирования: от DEV до PROD
https://habr.com/ru/companies/rtlabs/articles/577580/

PROD

Использование Portianer для управления платформой VMmanager
astraadmin@VMmanager:~$ sudo docker volume create portainer_data
astraadmin@VMmanager:~$ sudo docker run -d -p 8000:8000 -p 9443:9443 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:2.21.5

astraadmin@VMmanager:~$ sudo docker ps | grep 9443
[sudo] пароль для astraadmin:
6d85a11d8aa9   portainer/portainer-ce:2.21.5                                             "/portainer"             2 hours ago    Up 2 hours   0.0.0.0:8000->8000/tcp, :::8000->8000/tcp, 0.0.0.0:9443->9443/tcp, :::9443->9443/tcp, 9000/tcp                                                                                          portainer

