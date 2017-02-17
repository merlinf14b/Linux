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

# Config

## http://sabnzbd:8080/config/general/
```
# Maximum line speed
# Speed of Internet Service in MB
20M


# Percentage of line speed
50

# Article Cache Limit
1G
```


## http://sabnzbd:8080/config/folders/
```
# Permissions for completed downloads
777
```


## http://sabnzbd:8080/config/server/

### Server 0 - Main account
Priority 1
- [x] Optional

### Server 1 - Backup / Block Account
Priority 1
- [x] Optional


## http://sabnzbd:8080/config/categories/
Category | Priority | Processing | Folder/Path | Groups / Indexer tags
------------ | ------------ | ------------ | ------------ | ------------
movies | default | default | movies | movies*
sickrage | default | default | sickrage | 
tv | default | default | tv | tv*


## http://sabnzbd:8080/config/switches/

### Queue
- [x] Check before download
- [x] Abort jobs that cannot be completed
Detect Duplicate Downloads - Pause
Action when encrypted RAR is downloaded - Abort
Action when unwanted extension detected - Abort
Unwanted extensions ```exe, com, bat```

### Post processing
- [x] On failure, try alternative NZB
Cleanup extensions ```.nfo, .sfv, .nzb, .srr, .info, .idx, .txt, .db, .md5, .par2, .png, .1, .jpg, .jpeg, .url, .lnk, .html, htm, .ini, .bat, .com, .exe, .scr, .sample```