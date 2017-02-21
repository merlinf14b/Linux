# sickrage install on Ubuntu 16.10

```bash
apt-get update && apt-get dist-upgrade

apt-get install curl unrar-free git-core openssl libssl-dev python2.7

adduser installer

usermod -aG sudo installer

su - installer

curl https://raw.githubusercontent.com/SickRage/SickRage/master/contrib/debian-ubuntu-install.sh | sudo bash
```

```http://sickrage:8081/```

```bash
logout

deluser installer sudo

deluser --remove-home installer

reboot
```
