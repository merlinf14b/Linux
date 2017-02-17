```bash
apt-get update && apt-get dist-upgrade

apt-get install curl

echo deb https://downloads.plex.tv/repo/deb/ public main | sudo tee /etc/apt/sources.list.d/plexmediaserver.list

curl https://downloads.plex.tv/plex-keys/PlexSign.key | sudo apt-key add -

apt-get update

apt-get install plexmediaserver

apt-get install cifs-utils

mkdir /mnt/plex

nano ~/.smbcredentials
```

```bash
username=plex
password=XXXXXXXXX
```

```
chmod 600 ~/.smbcredentials

nano /etc/fstab
```

```
//nas/plex /mnt/plex cifs credentials=/root/.smbcredentials,iocharset=utf8,uid=1000,gid=1000 0 0
```

```
mount -a

cd /mnt/plex

ls

reboot
```

```http://plex:32400/```