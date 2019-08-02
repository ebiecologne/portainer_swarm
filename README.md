# Portainer with Traefik as Reverse-Proxy
* Just do a few things:
```bash
mkdir logs
touch logs/access.log
touch logs/traefik.log

mkdir content
touch content/acme.json
chmod 600 content/acme.json
```

* deploy portainer with traefik:
```
docker stack deploy -c docker-compose.traefik.portainer.yml portainer
```
* remove the stack:
```
docker stack rm portainer
```
* other commands:
```
docker service ps portainer_traefik
docker stack ps portainer
```
