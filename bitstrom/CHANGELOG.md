# Changelog

## 1.0.1

- The add-on no longer restarts every minute and a half. Its health check
  was refused (it asked `localhost`, which now means IPv6 first), so Home
  Assistant's watchdog kept restarting it.
- Stopping and updating the add-on is immediate: it shuts down cleanly
  instead of being killed after a timeout.

## 1.0.0

- **Bitstrom in the sidebar.** The add-on opens inside Home Assistant
  (ingress): from the sidebar or **Open web UI**, behind Home Assistant's
  sign-in, and also over https and Nabu Casa — away from home too. The
  address `http://<home-assistant>:17770` keeps working on the home network.
- **The dashboard card** ([Bitstrom card](https://github.com/yybd/bitstrom-card),
  in HACS) finds the add-on by itself, and can show the player bar alone or
  open on one type and collection.
- After an update, the browser loads the new app instead of keeping the old
  one.
- Jamendo: every track links to its page on Jamendo — in the results, the
  item menu and Now Playing.
- Search: HQ radio streams (Pulham's FLAC and 320k list); the Audiophile
  picks list is gone. **Add one item by URL** opens in the Search window,
  and every row to add says "Add …".
- Settings: a Privacy policy row.

## 0.1.21

- The sheet that asks which collection to add to also offers **Add to
  queue** (to the end of what Next steps through) and **Play now** (right
  after what plays), while a player is connected.
- Nothing is added twice: before the sheet opens, what is already in the
  library is found (any spelling of its address) and the sheet says in
  which collection; only new items are added.
- radio-browser shows once in Search: the radio-browser address you added
  as a radio source, not the built-in one beside it.

## 0.1.19

- **Add a radio station source** (was "Add radio address"): two more open
  station lists to add — moOde's station list and Recommended radio streams
  (deroverda). A station a source may block outside its country says so.
- A source or a station already added is not added twice; the screen says so.
- Stations whose address is a playlist (.pls / .m3u) now play on every
  player: the stream inside the playlist is handed over.
- UPnP / OpenHome players: an episode resumed from a position starts there,
  and a seek the player refuses while it opens the stream is asked again.
- Qobuz: sign-in keeps working when Qobuz changes its app id and keys.

## 0.1.18

- Eleven more languages: German, French, Spanish, Italian, Dutch, Japanese,
  Portuguese (Brazil), Polish, Russian, Arabic and Chinese, beside English
  and Hebrew. Settings → Language names the language in use.
- SomaFM is gone: its terms (September 2026) allow no third-party apps.
- "Custom radio directory" is now **Add radio address**. Under it, ready
  addresses to tap: radio-browser, Radio Paradise, KEXP, NTS, WFMU, the
  Icecast directory and the audiophile picks — an address saved there puts
  that source in Search. The built-in radio sources are no longer listed
  among the sources to add.
- Every radio directory you added (name, address, now-playing address)
  travels in the shared settings file to your other devices.

## 0.1.14

- Eleven more languages: German, French, Spanish, Italian, Dutch, Japanese,
  Portuguese (Brazil), Polish, Russian, Arabic and Chinese — beside English
  and Hebrew. The browser's language is picked up by itself; any other can be
  chosen under Settings → Language, which now names the language in use.
- Texts that named screens and buttons by old names now say what the app
  shows (Search, Local or network folders, Library file…).

## 0.1.12

- In the player, a Hebrew (or Arabic) line that fits sits on the left, like
  every other language; only a line too long to fit starts from the right
  and scrolls.

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
