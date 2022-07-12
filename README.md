# Pokestudio docker registry

Private Docker Registry

---

# Quick start

```bash
git clone git@github.com:DevPoke/docker-registry.git
cd docker-registry
# Configure you registry file
cp registry/config.yml.example registry/config.yml
# Configure your docker-compose env variables
cp .env.example .env
htpasswd -Bc registry/.htpasswd-users <username> <htpasswd>
```

# Docker login

```shell
docker login -u pokestudio registry.pokestudio.it
```

# Deploy

## 1) Docker compose

```shell
docker-compose up -d
```

## 2) Docker swarm

Create aliases `docker-stack` to maintain compatibility with docker-compose.

```shell
alias docker-stack='env $(cat .env | grep ^[A-Z] | xargs) docker stack'
alias docker-stack-deploy='docker-stack deploy --compose-file docker-compose.yml ${PWD##*/}'
```

```shell
docker-stack-deploy
```
