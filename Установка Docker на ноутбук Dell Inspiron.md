Соединение по ssh с ноутбуком
ssh -v -i "C:\Users\igorl\YandexDisk\Igor2024\id_rsa" liv@igor2024

Enter passphrase for key 'C:\Users\igorl\YandexDisk\Igor2024\id_rsa':

liv@igor2024:~$ sudo apt update
[sudo] пароль для liv:

liv@igor2024:~$ sudo reboot

liv@igor2024:~$ hostnamectl
 Static hostname: igor2024
       Icon name: computer-laptop
         Chassis: laptop
      Machine ID: 0e62da2ee1cd46f8bb0f8c348878ac2e
         Boot ID: 791c4f97db624f02b556ad75c8f0a3f6
Operating System: Ubuntu 22.04.4 LTS
          **Kernel: Linux 6.5.0-21-generic**
    Architecture: x86-64
 Hardware Vendor: Dell Inc.
  Hardware Model: Inspiron 3542

liv@igor2024:~$ docker -v
Docker version 25.0.4, build 1a576c5

liv@igor2024:~$ docker run -d -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer

