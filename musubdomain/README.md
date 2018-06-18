## mu subdomain

### start traefik container

```
docker run \
-d \
-p 8080:8080 \
-p 80:80 \
-p 443:443 \
-l "traefik.enable=false" \
-v /var/run/docker.sock:/var/run/docker.sock \
-v /opt/easyengine/traefik/traefik.toml:/etc/traefik/traefik.toml \
-v /opt/easyengine/traefik/acme.json:/etc/traefik/acme.json \
-v /opt/easyengine/traefik/endpoints:/etc/traefik/endpoints \
-v /opt/easyengine/traefik/certs:/etc/traefik/certs \
-v /opt/easyengine/traefik/log:/var/log \
-e CLOUDFLARE_EMAIL=mail@example.com \
-e CLOUDFLARE_API_KEY=<GLOBAL_API_KEY> \
--name ee_traefik easyengine/traefik
```
