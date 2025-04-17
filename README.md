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

**Docker**
Repo:
```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

App:
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo docker run hello-world
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










