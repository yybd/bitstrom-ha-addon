# Bitstrom

Your radio, podcasts and music library, played bit-perfect on the players in
your home.

## How it works

The add-on runs the Bitstrom server. Its web app (the **Open web UI**
button, or `http://<home-assistant>:17770`) is the full Bitstrom app: your
library, Search (radio directories, podcasts, streaming services, media
servers, music folders), and the player bar for whichever player you choose.

Players are controlled over your network; audio goes from the source straight
to the player, never converted. Music from folders is served to players by
the add-on's file server on port 17771.

## Configuration

| Option | Default | |
| --- | --- | --- |
| `library_dir` | `/share/bitstrom` | The folder holding `bitstrom-library.json` and `bitstrom-settings.json`. |

**Sharing with your other devices.** The phone and desktop apps keep the
library in a folder you choose. Make it the same folder everywhere and every
device shares one library and one set of settings (players, media servers,
Search sources), kept in step continuously. With Home Assistant, a folder
under `/share` that is synced with your other devices works well (for
example with the Samba share add-on, Syncthing or Nextcloud). Passwords and
keys stay where they were entered.

**Music folders.** Folders under `/media` (read-only) and `/share` can be
added in the app under Search → Add or edit sources → Music folders.

## Network

The add-on uses the host network: players and media servers are found by
multicast (SSDP / mDNS), and players must reach the file server. Ports:
`17770` (app and API) and `17771` (file server).

## Support

Issues and questions: https://github.com/yybd/bitstrom-ha-addon/issues
