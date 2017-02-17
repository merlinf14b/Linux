# iperf 3 install on Ubuntu 16.10

apt-get update && apt-get dist-upgrade

apt-get install iperf3

adduser iperf --disabled-login

nano /etc/systemd/system/iperf3.service

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

systemctl daemon-reload

systemctl start iperf3

systemctl status iperf3

systemctl enable iperf3

reboot
