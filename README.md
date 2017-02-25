# Docker up Drupal env.
Create a Drupal docker container for your development env.

### Install docker && docker compose
please refer to these tutorials:
* install docker (https://docs.docker.com/installation/ubuntulinux/)
```shell
curl -sSL https://get.docker.com/ | sh
```
* install docker compose (https://docs.docker.com/compose/install/)
```shell
curl -L https://github.com/docker/compose/releases/download/1.6.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
```

### Pull docker image
```shell
docker pull ivan-berezhnov/docker-up-drupal
```

### Clone && Edit docker-compose.yml
```shell
git clone https://github.com/ivan-berezhnov/docker-up-drupal.git
```
```docker-compose.yml``` then edit the file with you own paths and ports.

### Start your containers
There are only two containers to run. web container ( includes everything except your database ),
and mariadb container.
```shell
sudo docker-compose up -d
```

# Edit down text #
### SSH into the container:
```shell
docker exec -it $PROJECT_NAME-drupal bash
```