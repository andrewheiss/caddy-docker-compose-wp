# Docker Compose + WordPress + Caddy

This shows how to configure Caddy to serve both static HTML sites and a WordPress site, all through Docker Compose.

All Docker Compose-related things (persistent data folders, environment variables, etc.) live inside `server-stuff/*`.

Static HTML sites live inside `sites/*`, and they can be configured as standalone sites through Caddy settings (see `server-stuff/caddyfiles/`)

To keep WordPress PHP files outside of the static HTML folder, WordPress itself lives in `server-stuff/wordpress`. It's also mapped to a different location inside the Caddy and PHP containers (`/wordpress/` instead of `/var/www/html/`).

This example creates three sites:

- https://example.localhost
- https://data.example.localhost
- https://anothersite.localhost
