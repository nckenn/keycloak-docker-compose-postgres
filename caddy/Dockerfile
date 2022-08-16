ARG CADDY_VERSION=2

# Build Caddy
FROM caddy:${CADDY_VERSION}-builder-alpine AS app_caddy_builder

RUN xcaddy build

# Caddy image
FROM caddy:${CADDY_VERSION} AS app_caddy

COPY --from=app_caddy_builder /usr/bin/caddy /usr/bin/caddy
COPY Caddyfile /etc/caddy/Caddyfile