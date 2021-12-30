# docker-registry

Private Docker Registry

---

# Setup a docker image registry

Follow the guide: https://linuxhint.com/setup_own_docker_image_repository/

# Quick start

```bash
git clone git@github.com:DevPoke/docker-registry.git
cd docker-registry
htpasswd -Bc registry/htpassword registry-admin
docker-compose up -d
```
