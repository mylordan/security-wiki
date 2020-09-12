
# How to enable ssh 22

### 1 - Edit /etc/ssh/ssh_config

```
$: sudo vi /etc/ssh/sshd_config

### Remove '#' for below configuration items:
PasswordAuthentication yes
Port 22

```

### 2 - Restart SSH service and enable auto start when server reboot

```
$: sudo /etc/init.d/ssh start

$: sudo update-rc.d ssh enable

$: systemctl status ssh

```

### 3 - Check if ssh is working

```

$: netstat -lnt

```