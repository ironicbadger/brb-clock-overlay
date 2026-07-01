# KTZ BRB Overlay

Dockerized OBS browser-source overlay for the KTZ Systems BRB scene.

It serves a full-screen 1920x1080 BRB page with:

- dark graph-paper background with orange accents
- camcorder-style `REC` clock/date panel
- rotating family-safe intermission lines
- embedded JetBrains Mono ExtraBold for the main `BRB` text

## Run

```sh
docker compose up -d
```

The overlay is served on:

```text
http://127.0.0.1:8787/
```

Use that URL as an OBS Browser Source at `1920x1080`.

## Extra Overlay

A smaller clock-only source is also available:

```text
http://127.0.0.1:8787/clock.html
```

## OBS Refresh

After editing the HTML/CSS, right-click the OBS Browser Source, open **Properties**, and use **Refresh cache of current page**.

## Files

- `html/index.html` - full BRB scene
- `html/clock.html` - standalone REC/date/time overlay
- `html/fonts/` - embedded font asset for OBS browser compatibility
- `compose.yaml` - nginx container bound to localhost
- `nginx.conf` - static server config with no-cache headers
