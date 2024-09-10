# Install SSH on VM

```
sudo apt update
sudo apt install openssh-server
sudo apt install openssh-client
```

# Start/Enable SSH Service

```
sudo systemctl start ssh
sudo systemctl enable ssh
sudo systemctl status ssh
```
- make sure its active

# Ensure Firewall inside VM allows SSH Connections

```
sudo ufw allow ssh
sudo ufw enable
```

# Network Configuration In VirtualBox (NAT + port forwarding)

- Shut Down VM and Go to settings -> Network -> Advanced -> Port Forwarding
- Add new port forwading rules 

![image](https://github.com/user-attachments/assets/9eacb3d1-64f9-4e24-95ea-8a5956d1e12f)

# Testing SSH Connection

- try running `ssh -p 2222 <username>@localhost` on host's machine to ssh into vm
- To find vm username run `hostname` in vm
