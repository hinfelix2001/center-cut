# Felix Vocal Remover

Free vocal remover by Felix. Split a stereo song into **vocals, drums, bass and other** right in your browser, then remix it: karaoke, acapella, drumless or bassless practice tracks.

- HD mode: AI separation on a free GPU server. Quick mode: runs fully in the browser, nothing uploaded.
- 4-stem mixer with volume, mute and solo
- Quick mixes: Original, No vocals, Vocals only, No drums, No bass, Drums only, Bass only
- Save the current mix or all four stems as WAV
- Key & BPM finder: key, Camelot code, tempo and energy for the loaded song or a whole batch of files, tap tempo, save results as CSV

## HD mode (AI server)

HD mode sends the song to a free Hugging Face ZeroGPU Space (hinfelix2232/felix-vocal-remover) that runs Demucs (HTDemucs v4 by Meta, MIT) and returns four MP3 stems. Uploads are deleted automatically within an hour. Server code is in the Space.

## Quick mode: how it works

1. **Drums:** harmonic/percussive separation (median filtering of the spectrogram) pulls out short hits.
2. **Vocals:** from the tonal part, frequency bins that are identical in both channels (center-panned) are taken as the lead vocal.
3. **Bass / Other:** the rest is split at an adjustable bass frequency.

The four stems always add back up to the original. Best results come from studio stereo mixes; mono files can't have their vocals separated.

## Run it

Open `index.html` in Chrome, Edge or Firefox. No build step, no server.
