docker run --name self-cert-test \
      -v ~/self-cert/index.html:/usr/share/nginx/html/index.html:ro -d \
      -v ~/self-cert/certs/nginx-selfsigned.crt:/etc/ssl/certs/nginx-selfsigned.crt \
      -v ~/self-cert/certs/nginx-selfsigned.key:/etc/ssl/private/nginx-selfsigned.key \
      -l "traefik.enable=true" \
      -l "traefik.basic.port=80" \
      -l "traefik.basic.protocol=http" \
      -l "traefik.secure.port=443" \
      -l "traefik.secure.protocol=https" \
      -l "traefik.docker.network=site-network" \
      -l "traefik.frontend.entryPoints=http,https" \
      -l "traefik.frontend.rule=Host:site1.test,www.site1.test" \
      -l "traefik.frontend.redirect.regex=^https?://www.site1.test/(.*)" \
      -l "traefik.frontend.redirect.replacement=https://site1.test/$${1}" \
      nginx:dharmin

