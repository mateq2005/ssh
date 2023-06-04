# SSH

### Enable SSH on Ubuntu

```
sudo apt-get update
sudo apt-get install openssh-server
```

```
sudo ufw allow ssh
sudo ufw status
```

```
sudo service ssh status
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
PermitRootLogin_yes
```

```
sudo systemctl restart sshd.service
```
