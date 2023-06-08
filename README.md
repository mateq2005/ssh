# SSH

### Enable SSH on Ubuntu

```
sudo apt-get update
sudo apt-get install openssh-server
```

```
systemctl start openssh-server
systemctl enable openssh-server
```

### Log Into Remote Server With SSH

```
ssh username@IPv4 -p22
```

### SSH Configuration Option

```
sudo nano /etc/ssh/sshd_config
```

```
Port 22

PasswordAuthentication no

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
sudo systemctl restart sshd.service
```

*tested*
