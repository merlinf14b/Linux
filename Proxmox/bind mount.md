# Bind mount from host into container

### On container
```bash
mkdir /mnt/storage
```

### On host
```bash
# nano /etc/pve/lxc/[CONTAINER ID].conf

nano /etc/pve/lxc/100.conf


# add mount point
# mp0: [HOST PATH],mp=[CONTAINER PATH]

mp0: /mnt/storage,mp=/mnt/storage
```

### Restart Container