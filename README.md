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
docker-compose up -d
```
