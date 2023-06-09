# SSH

### Installing OpenSSH

```
sudo apt-get update
sudo apt-get install openssh-server -y
```

```
systemctl start sshd
systemctl status sshd
```

### Log Into Remote Server With SSH

```
ssh username@IPv4 -p22
```

### SSH Configuration Options

```
sudo nano /etc/ssh/sshd_config
```

```
Port 22

PasswordAuthentication yes
PermitRootLogin yes

MaxAuthTries 6 
MaxSessions 10
LoginGraceTime 2m

AllowUsers username
DenyUsers username
AllowGroups group
DenyGroups group 

Banner /etc/issue.net
```

### Restarting SSH Service 
```
sudo systemctl restart sshd
```

*tested*
