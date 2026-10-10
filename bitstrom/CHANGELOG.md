# Changelog

## 0.1.3

- Phones can keep their settings in step through the add-on: in the
  Bitstrom app on a phone, **Settings → Bitstrom server → Sync settings
  through this server** (off until you turn it on). Players, media servers,
  Search sources and service settings meet here, even when each device keeps
  its settings file somewhere else (iCloud on one, Google Drive on another).
  Passwords and tokens stay on each device.
- The phone app also finds media servers itself now; an iPhone, which cannot
  scan the network, asks the add-on to scan for it.

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
