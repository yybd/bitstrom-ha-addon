# Changelog

## 0.1.11

- Internet radio shows what is playing now, where the station says: a radio
  directory of your own is asked for its now-playing feed (set its address
  in the directory's settings, `{uuid}` for the station — or leave it empty
  and the usual place is tried), and any station whose stream server has a
  status page (Icecast, SHOUTcast) shows the song from there.
- It shows on every device that watches the add-on, also when the station
  was started from another device or app.
- A song the feed itself marks as out of date (a live broadcast while the
  studio is on air) is not shown as playing.

## 0.1.8

- The library syncs through the add-on too: a phone with **Sync settings
  and library through this server** on sends its songs, stations, podcasts
  and collections, and gets everyone else's — even when each device keeps
  its library somewhere else (iCloud, Google Drive).
- When separate libraries first meet, the same song (by its address) and the
  same collection (by name) become one.

## 0.1.7

- Played through the add-on (the browser, the desktop app), a song started
  from a list hands the player the songs that follow, so it plays on by
  itself — as it already did from the phone.

## 0.1.6

- Songs handed to a player are named in its queue before they play (MPD,
  LMS, Sonos, Chromecast, OpenHome), not shown as bare addresses.
- How many songs a player will still play comes from the player itself, so
  every device and browser that shows it sees the same count.

## 0.1.5

- OpenHome renderers (Linn, upmpdcli with OpenHome on, Lumin…) are handed
  the songs into their own playlist and play on by themselves; one that
  speaks only OpenHome is found and accepted too.

## 0.1.4

- The same player added on two devices before they shared settings showed
  twice; the records are now folded into one on every device, keeping its
  password and the player in use.
- Players with a queue of their own (MPD, LMS, Sonos, Chromecast, and Home
  Assistant entities that queue) are handed the songs that follow, so they
  play on by themselves.

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
