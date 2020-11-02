# Requisites

### Docker
```bash
sudo apt-get update
sudo curl -sSL https://get.docker.com | sh
sudo usermod -aG docker pi
sudo reboot
```

### Docker-compose
```bash
sudo apt-get install -y libffi-dev libssl-dev python3 python3-pip
sudo apt-get remove python-configparser
sudo pip3 -v install docker-compose
```

# Running

Modify .env with your configuration and run the following:
```
docker-compose up -d
```