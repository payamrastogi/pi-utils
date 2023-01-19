- Verify status
```shell
sudo ufw status
```

- Setting up default UFW policy
```shell
sudo ufw default allow outgoing
sudo ufw default deny incoming
```

- How to allow incoming SSH from specific IP address
```shell
sudo ufw allow from {IP_ADDRESS_HERE} to any port 22
```

- View all added rules
```shell
sudo ufw show added
```

- Enable UFW firewall
```shell
sudo ufw enable
```

###### References
- https://www.cyberciti.biz/faq/ufw-allow-incoming-ssh-connections-from-a-specific-ip-address-subnet-on-ubuntu-debian/
- https://www.cyberciti.biz/faq/how-to-setup-a-ufw-firewall-on-ubuntu-18-04-lts-server/