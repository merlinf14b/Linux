# sabnzbd install on Ubuntu 16.10

```bash
apt-get update && apt-get dist-upgrade

apt-get install software-properties-common

apt-add-repository multiverse && apt-get update

apt-get install sabnzbdplus

adduser sabnzbd --disabled-login

nano /etc/default/sabnzbdplus
```

```bash
USER=sabnzbd
HOST=0.0.0.0
PORT=8080
```

```bash
service sabnzbdplus start

service sabnzbdplus status

reboot
```

```
http://sabnzbd:8080/
```