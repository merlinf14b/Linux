# iperf 3 install on Ubuntu 16.10

```bash
apt-get update && apt-get dist-upgrade
```

```bash
apt-get install iperf3
```

```bash
adduser iperf --disabled-login
```

```bash
nano /etc/systemd/system/iperf3.service
```

```bash
[Unit]
Description=iperf3 Service
After=network.target

[Service]
Type=simple
User=iperf
ExecStart=/usr/bin/iperf3 -s
Restart=on-abort

[Install]
WantedBy=multi-user.target
```

```bash
systemctl daemon-reload
```

```bash
systemctl start iperf3
```

```bash
systemctl status iperf3
```

```bash
systemctl enable iperf3
```

```bash
reboot
```