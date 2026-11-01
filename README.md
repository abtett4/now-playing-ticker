# Now Playing ticker

A live "now playing" display for my Spotify listening, drawn as a grid of LEDs in the browser with [p5.js](https://p5js.org/).
It mirrors a physical MAX7219 LED matrix ticker I run on a Raspberry Pi.

- **Live data** comes from a small Cloudflare Worker that asks Spotify what's playing (at most once every 15 seconds) and returns only the song, artist and album art.
- **Lettering** uses the CP437 8×8 font from [luma.core](https://github.com/rm-hull/luma.core) (MIT licence, © 2017-2021 Richard Hull and contributors), the same font as the hardware ticker.
- **Other scripts:** accents are stripped, Cyrillic, Greek and Korean are romanized, and Japanese and Chinese are drawn from your system fonts.
- **Album art** is sampled down to a 24×24 grid and ripples in when the song changes. With reduced motion turned on, nothing scrolls or ripples.
