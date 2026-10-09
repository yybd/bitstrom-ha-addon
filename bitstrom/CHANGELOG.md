# Changelog

## 0.1.2

- The add-on announces itself on your network, so the Bitstrom app on a
  phone finds it and uses it to discover players — every kind, including
  the DLNA, Sonos, HEOS and LMS players an iPhone cannot find by itself.

## 0.1.1

- The app now listens on port **17770** (was 8080, often taken on a Home
  Assistant host): open `http://<home-assistant>:17770`.
- The Log tab shows what the server does (start-up, the port, errors); a port
  already in use is said plainly instead of a silent restart loop.

## 0.1.0

- First release: the Bitstrom server as a Home Assistant add-on — library,
  players (MPD, LMS, DLNA, Sonos, BluOS, WiiM, Chromecast…), radio, podcasts,
  media servers and music folders, in English and Hebrew.
