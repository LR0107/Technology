## Remote Connection from Windows to Linux

## Linux

### Install OpenSSH Server

```bash
sudo apt install openssh-server
```

### Start SSH Service

`sudo systemctl start sshd`

### Check SSH Status

`sudo systemctl status sshd`

### Check IP Address

`ifconfig   # requires net-tools to be installed`

## Windows

### Test Network Connectivity

`ping <IP_ADDRESS>`

### Connect via SSH

`ssh <username>@<server_ip_address>`
