# Homelab Scripts

Some scripts and notes that I use to keep my homelab running

## Docker Run

Setup Watcher, auto update containers

```bash
docker run -d \
--name watchtower \
--restart=unless-stopped \
-v /var/run/docker.sock:/var/run/docker.sock \
containrrr/watchtower
```

Setup Portainer, GUI for Docker

```bash
docker volume create portainer_data
```

```bash
docker run -d -p 8000:8000 -p 9443:9443 \
--name portainer \
--restart=unless-stopped \
-v /var/run/docker.sock:/var/run/docker.sock \
-v portainer_data:/data \
cr.portainer.io/portainer/portainer-ce
```
