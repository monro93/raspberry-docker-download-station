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

Modify .env with your configuration, comment services that you don't want in docker-compose.yaml and run the following:
```
docker-compose up -d
```

# Services

## JDownloader
Set email and login with the following command:
```bash
docker exec pidownload-jdownloader configure email@email.com password
```

## Convert videos
In order to be convert all the videos that you have downloaded to standard file formats, add the following script to a cron:
```
docker run --rm -t -v downloads_folder:/media jaymoulin/rpi-plex-video-converter
```