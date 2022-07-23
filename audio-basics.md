
Audio Setup
===========

Basics About Audio
------------------

Version 1.0.0 (2022-07-23)

The audio loudness scale knows about three primary units:

- dB   (DeciBel, relative to a base value)
- dBFS (DeciBel relative to Full Scale)
- LUFS (Loudness Unit relative to Full Scale)
- RMS  (Root Mean Square)

The relation of the absolute values is that `dbFS == LUFS ~~ RMS`. LUFS
is about the perceived loudness according to the Fletcher Munson curve
while RMS is a plain mathematical average loundness.

The audio loudness scale can be somewhat segmented in 3 dB steps like this:

```txt
dBFS                             NOISE   VOICE
   0 ==== very loud
-  3
-  6
-  9                                     X
- 12 ==== loud                           X
- 15                                     # (-14 dBFS: target for YouTube / Spotify)
- 18                                     # (-16 dBFS: target for Apple Music)
- 21                                     # (-23 dBFS: target for EBU R128 / Cinema / TV)
- 24 ==== regular                        #
- 27                                     X
- 30                                     X
- 33                                     X
- 36 ==== quietly                        X
- 39                                     X
- 42                                     X
- 45                                     X
- 48 ==== very quietly                   X
- 51
- 54
- 57
- 60 ==== Noise Floor Peeks      X
- 63                             X
- 66                             X
- 69                             X
- 72 ==== Noise Floor Majority   X
- 75                             X
- 78                             X
- 81                             X
- 84 ====                        X
- 87                             X
- 90                             X
- 93                             X
- 96 ====                        X
- 99                             X
-102                             X
```

