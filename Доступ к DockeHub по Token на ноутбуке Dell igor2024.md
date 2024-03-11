liv@igor2024:~$ docker login -u igorlytkin
Password:
WARNING! Your password will be stored unencrypted in /home/liv/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
liv@igor2024:~$ cat /home/liv/.docker/config.json
{
        "auths": {
                "https://index.docker.io/v1/": {
                        "auth": "*XXX*"
                }
        }
}

liv@igor2024:~$ ls -la /home/liv/.docker/
итого 12
drwx------  2 liv liv 4096 мар  9 10:31 .
drwxr-x--- 30 liv liv 4096 мар  9 10:31 ..
-rw-------  1 liv liv  135 мар  9 10:31 config.json

