# DO-Docker
Experimental Docker install on a Digital Ocean VPS, evaluating before updating main Droplet.

---

## Rebuild Droplet

Spare droplet, rebuild on DO website.

> Ubuntu 24.04 LTS

Login as root.

Reset password.

Create own user.

```bash
adduser yourname
usermod -aG sudo yourname
```

Use PuTTYgen to create a new keypair.

Private Key -> PuTTY
Public Key -> /home/yourname/.ssh/authorized_keys

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl git unzip ufw
```

Docker

```bash
curl -fsSL https://get.docker.com | sudo sh

sudo docker version

sudo usermod -aG docker jonathan
newgrp docker

sudo apt install -y docker-compose-plugin
```

Testing it with WriteFreely
https://hub.docker.com/r/algernon/writefreely  

Adding Caddy
https://hub.docker.com/_/caddy/  










