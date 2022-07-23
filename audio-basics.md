
Audio Setup
===========

Basics About Audio
------------------

Version 1.0.0 (2022-07-23)

First, see [How Sound Works](https://www.youtube.com/watch?v=mjv7O0KS1ug)
for the basics. Then remember that
persons perceive loudness in a way which is more a logarithmic than linear
fashion. The Decibel (dB, 1/10 of a Bel) unit accounts for this.
See [Decibels In Audio](https://www.youtube.com/watch?v=F4r3WI-JXlc)
for all the basics about Decibel.

Keep also in mind that Decibel for Power is originally calculated `dB = 10 *
log(Power2/Power1)` while Decibel for Voltage and Sound Pressure (our case)
is calculated as `dB = 20 * log(Value2/Value1)`. So be careful when
reading about dB in general and applying it in the context of audio.

The audio field knows and uses multiple primary units:

- dB   (DeciBel)
- dBFS (DeciBel relative to Full Scale)
- LU   (Loudness Unit)
- LUFS (Loudness Unit relative to Full Scale)
- RMS  (Root Mean Square)

The dB/LU is a relative unit with 1 dB equal to 1 LU, the others are absolute units.
The relation of the absolute values is that `dbFS == LUFS ~~ RMS`. LUFS
is about the perceived loudness according to the [Fletcher Munson curve](https://en.wikipedia.org/wiki/Equal-loudness_contour)
while RMS is a plain mathematical average loundness.
Hence, primarily use LUFS when dealing with loudness.

The dB/LU has known amplitude/pressure ranges:

- Near-Zotal Silence (Threshold of Hearing): 0 dB
- Breathing: 10 dB
- Whispering: 15 dB
- Library Room: 45 dB
- Conversation: 60 dB
- Noisy Restaurant: 90 dB
- Jet Engine: 120 dB
- Threshold of Pain: 140 dB
- Balloon Popping: 157 dB

The speed of sound is 343 m/s = 0.343 m/ms = 34.3 cm/ms, which means
that in one millisecond (ms), sound travels about 34 cm in a usual room
of 20 degree celcius. This means that when a speaker is 1 meter away
from your microphone, a ducking filter should have a maximum attack of 3
ms.

Because of the logarithmic way of hearing, the well-known dB ratios for sound are:

- 1:10 -20 dB (ten times as quiet)
- 1:2   -6 dB (double as quiet)
- 1:1    0 dB
- 2:1   +6 dB (double as loud)
- 10:1 +20 dB (ten times as loud)

LUFS is usually measured over different time ranges:

- LUFS m / ML (Momentary Loudness): 400 ms
- LUFS s / STL (Short Term Loudness): 3 s
- LUFS i / IL (Integrated Loudness): total (entire audio track)

The audio volume scale can be somewhat segmented in 3 dB steps like this
and noise and voice areas marked on it:

```txt
dBFS                             NOISE   VOICE
   0 ==== very loud
-  3                                     X
-  6                                     X
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
- 51                                     X
- 54                                     X
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

For even more Audio details, check out
the [Audio University](https://www.youtube.com/hashtag/audiouniversity).

