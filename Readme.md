# MySQL with Docker

### Config Docker (Ubuntu 22.04)

Install docker
```bash
sudo apt update
sudo apt upgrade
sudo apt install docker.io -y
```

Install docker compose
```bash
DOCKER_CONFIG=/usr/local/lib/docker
mkdir -p $DOCKER_CONFIG/cli-plugins
sudo curl -SL https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-x86_64 -o $DOCKER_CONFIG/cli-plugins/docker-compose
```
```bash
sudo chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose
```

To check
```bash
docker -v
docker compose version
```

Fix Docker Permission
```bash
sudo groupadd docker
sudo usermod -aG docker $USER
sudo groups $USER
```

---

### Run MySQL
Docker Compose Install MySQL
```bash
docker compose up -d
```
