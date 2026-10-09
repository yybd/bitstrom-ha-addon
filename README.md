# Bitstrom — Home Assistant add-on repository

Bitstrom keeps your internet radio, podcasts and music library in one place
and plays them **bit-perfect** on the players in your home: MPD (moOde,
Volumio…), LMS / Squeezelite, DLNA renderers, Sonos, BluOS, WiiM / LinkPlay,
HEOS, Chromecast and Home Assistant media players. Nothing is converted —
each player gets the music exactly as it is.

This repository holds the add-on. The same server runs in the Bitstrom
desktop app (macOS, Windows) and as a Docker image.

## Install

1. In Home Assistant: **Settings → Add-ons → Add-on Store → ⋮ → Repositories**.
2. Add `https://github.com/yybd/bitstrom-ha-addon` and close the dialog.
3. Find **Bitstrom** in the store, open it and press **Install**.
4. On the **Configuration** tab, check the library folder (default
   `/share/bitstrom`), then **Start**.
5. Press **Open web UI** (or browse to `http://<home-assistant>:8080`).

See [the add-on documentation](bitstrom/DOCS.md) for details.

[![Open your Home Assistant instance and show the add add-on repository dialog.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fyybd%2Fbitstrom-ha-addon)
