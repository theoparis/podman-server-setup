FROM docker.io/caddy:builder-alpine AS builder

# Add caddy plugins here
RUN xcaddy build

FROM docker.io/caddy:alpine

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
