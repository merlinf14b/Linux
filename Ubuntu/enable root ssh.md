```bash
sed -i 's/prohibit-password/yes/' /etc/ssh/sshd_config

systemctl restart sshd
```