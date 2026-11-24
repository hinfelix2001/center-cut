# Center Cut

Split a stereo song into **vocals, drums, bass and other** right in your browser, then remix it: karaoke, acapella, drumless or bassless practice tracks.

- Nothing is uploaded. All processing runs locally in the browser.
- 4-stem mixer with volume, mute and solo
- Quick mixes: Original, No vocals, Vocals only, No drums, No bass, Drums only, Bass only
- Save the current mix or all four stems as WAV

## How it works

1. **Drums:** harmonic/percussive separation (median filtering of the spectrogram) pulls out short hits.
2. **Vocals:** from the tonal part, frequency bins that are identical in both channels (center-panned) are taken as the lead vocal.
3. **Bass / Other:** the rest is split at an adjustable bass frequency.

The four stems always add back up to the original. Best results come from studio stereo mixes; mono files can't have their vocals separated.

## Run it

Open `index.html` in Chrome, Edge or Firefox. No build step, no server.
