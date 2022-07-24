
Audio Setup
===========

Basics About Audio
------------------

Version 1.0.0 (2022-07-23)

First, see [How Sound Works](https://www.youtube.com/watch?v=mjv7O0KS1ug),
[Properties of a Sound Wave](https://www.youtube.com/watch?v=KUMI9sqD6vc),
and [Decibels Explained](https://www.youtube.com/watch?v=F4r3WI-JXlc)
of the [Audio University](https://www.youtube.com/hashtag/audiouniversity)
for all the basics. Let us recap all those essential basics:

1. Sound is vibration of material, usually air particles.

2. Sound travels as waves of accoustical energy --
   recurring air pressure changes, alternating between
   high/positive/compression and low/negative/rarefaction.

3. Sound can be visualized as a sine-like curve on a diagram where the
   x-axis is the time and the y-axis is the air pressure.

4. Phase (of the curve) is measured in degrees from 0 (zero), over 90
   (maximum positive), 180 (zero), 270 (maximum negative), to 360 (zero).

5. Frequency (of the curve) is how many Phase cycles (0 to 360) occur
   per second (cps, cycles per second). Frequency is measured in Hertz (Hz)
   with 1 cps equal to 1 Hz. Human range of hearing is from 20 Hz to 20,000
   Hz. Higher Frequency corresponds to higher musical Pitch. If Frequency
   is doubled, musical Pitch increases by one Octave.

5. Period (of the curve) is the time to complete a Phase (0 to 360),
   measured in time (usually ms). A sound wave of 1 Hz has a Period of 1
   second, a sound wave of 2 Hz has a Period of 0.5 seconds.

6. Wavelength (of the curve) is the physical distance to complete a
   Phase (0 to 360), measured in meters. Wavelength = (Speed of Sound) /
   Frequency.

7. The Speed of Sound is 1130 ft/s = 344 m/s = 0.344 m/ms = 34.4 cm/ms,
   which means that in one millisecond (ms), sound travels about 34 cm in
   a usual room of 15-20 degree celcius. This means that when a speaker is
   1 meter away from your microphone, the ducking filter should have an
   attack of no more than 3 ms.

8. Amplitude is the extend of air pressure changes and is the range
   on the y-axis of the curve, originally measured in Pascal (ps, force
   per square meter), but, because of the logarithmic scale of the
   human hearing, in practice it is measured in Decibel (dB SPL), a
   logarithmic scale mapped onto the linear Pascal scale.

9. Decibel (Sound Pressure Level) (dB SPL) has known ranges:
    - Near-Zotal Silence (Threshold of Hearing): 0 dB SPL
    - Breathing: 10 dB SPL
    - Whispering: 15 dB SPL
    - Library Room: 45 dB SPL
    - Speech/Conversation: 60 dB SPL
    - Music: 80 dB SPL
    - Noisy Restaurant: 90 dB SPL
    - Jet Engine: 120 dB SPL
    - Threshold of Pain: 120/140 dB SPL
    - Balloon Popping: 157 dB SPL

10. The human way of hearing: as sound pressure increases, more and more
    power is required to create the same perceived(!) increase in loudness.
    The Decibel unit accounts for this.
    Because of this logarithmic way of human hearing, the well-known dB SPL ratios for sound are:
    - 1:10 -20 dB SPL (ten times as quiet)
    - 1:2   -6 dB SPL (double as quiet)
    - 1:1    0 dB SPL
    - 2:1   +6 dB SPL (double as loud)
    - 10:1 +20 dB SPL (ten times as loud)

11. The Decibel is 1/10 of a Bel and a power ratio between two values.
    Keep in mind that Decibel for Power is originally calculated `dB
    = 10 * log(Power-Measured / Power-Reference)` while Decibel for
    Voltage and Sound Pressure (our context) is calculated as `dB = 20 *
    log(Value-Measured / Value-Reference)`. So be careful when reading
    about dB in general and applying it in the context of audio.

12. In audio there are multiple absolute units:
    - dB SPL (Decibel relative to Sound Pressure Level)
    - dB FS  (Decibel relative to Full Scale)
    - LUFS   (Loudness Unit relative to Full Scale)
    - RMS    (Root Mean Square)
    The relation of the absolute units is db FS == LUFS ~~ RMS.
    The dB/LU is a relative unit with 1 dB = 1 LU.
    LUFS is about the perceived loudness according to the [Fletcher
    Munson curve](https://en.wikipedia.org/wiki/Equal-loudness_contour)
    while RMS is a plain mathematical average loundness. Hence,
    primarily use LUFS when dealing with loudness.

13. LUFS is usually measured over different time ranges:
    - LUFS m / ML  (Momentary Loudness): 400 ms
    - LUFS s / STL (Short Term Loudness): 3 s
    - LUFS i / IL  (Integrated Loudness): total (entire audio track)

14. Different organizations focus on different target loudness:
    - Netflix (Dialog): -27 LUFS i
    - EBU R128 (Cinema, TV): -23 LUFS i
    - EBU R128 S1 (TV): -23 LUFS i, -18 LUFS s
    - Apple Music / Apple Podcast: -16 LUFS i
    - Deezer: -15 LUFS i
    - Amazon Music: -14 LUFS i
    - YouTube: -14 LUFS i
    - Spotify: -14 LUFS i
    - Spotify Loud: -11 LUFS i
    Hence, in practice a useful target loudness is to follow EBU R128 S1 and try to reach
    -18 LUFS s and -23 LUFS i.

The audio volume scale can be somewhat segmented in 3 dB steps like this
and noise and voice areas marked on it for a reference configuring
certain [Audio Parameters](audio-params.md):

```txt
dBFS/LUFS                        NOISE   VOICE
   0 ==== very loud
-  3                                     X
-  6                                     X
-  9                                     X
- 12 ==== loud                           X
- 15                                     X
- 18                                     ## (-18 LUFS s: EBU R128 S1)
- 21                                     ##
- 24 ==== regular                        ## (-23 LUFS i: EBU R128 S1)
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

