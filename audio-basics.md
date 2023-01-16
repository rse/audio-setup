
Audio Basics
============

Version 1.1.3 (2023-01-07)

First, see [How Sound Works](https://www.youtube.com/watch?v=mjv7O0KS1ug),
[Properties of a Sound Wave](https://www.youtube.com/watch?v=KUMI9sqD6vc),
and [Decibels Explained](https://www.youtube.com/watch?v=F4r3WI-JXlc)
of the [Audio University](https://www.youtube.com/hashtag/audiouniversity)
plus the [Fundamentals of Audio Engineering](https://www.reddit.com/r/audioengineering/wiki/fundamentals/)
and the [Audio Engineering FAQ](https://www.reddit.com/r/audioengineering/wiki/faq/)
of the [Reddit Audio Engineering Community](https://www.reddit.com/r/audioengineering/)
plus the excellent book [Web Audio API](https://webaudioapi.com/book/Web_Audio_API_Boris_Smus.pdf)
for all the basics. Let us recap all those essential basics:

- **Sound** is a vibration of material, usually of air particles.
  Sound travels as waves of accoustical energy, i.e.,
  sound is based on recurring air pressure changes, alternating between
  high/positive/compression/pushed and low/negative/rarefaction/pulled.
  Sound can be visualized as a sine-like curve on a diagram where the
  x-axis is the time and the y-axis is the air pressure.

- **Phase** of sound is measured in degrees from 0 (zero), over 90
  (maximum positive), 180 (zero), 270 (maximum negative), to 360 (zero).

- **Period** of sound is the time to complete a Phase (from 0 to 360 degree),
  measured in time (usually ms). A sound wave of 1 Hz has a Period of 1
  second, a sound wave of 2 Hz has a Period of 0.5 second.

- **Frequency** of sound is how many Phase cycles (from 0 to 360 degree) occur
  per second (cycles per second, cps). Frequency is measured in *Hertz*
  (Hz) with 1 cps = 1 Hz. Human range of hearing is from 20 Hz to 20,000
  Hz. Higher Frequency corresponds to higher musical Pitch. If Frequency
  is doubled, musical Pitch increases by one Octave (a logarithmic unit
  for ratios between frequencies, with one Octave corresponding exactly
  to the doubling of Frequency).

- **Speed** of sound is 1130 ft/s = 344 m/s = 0.344 m/ms = 34.4 cm/ms,
  which means that in one millisecond (ms), sound travels about 34 cm in
  a usual room of 15-20 degree celcius. This means in practice that when
  a speaker is 1 meter away from your microphone, the ducking filter
  should have an attack of no more than 3 ms.

- **Wavelength** of sound is the physical distance to complete a
  Phase (from 0 to 360 degree), measured in meters. As a formula:
  Wavelength = Speed / Frequency.

- **Amplitude** is the extend of air pressure changes, originally
  measured in Pascal (ps, force per square meter), but, because of the
  logarithmic scale of the human hearing, in practice is measured in
  Decibel at Sound Pressure Level (dB SPL) -- a logarithmic scale mapped
  onto the linear Pascal scale.

- **Polarity** is the pushing and pulling of air in a Phase.
  When the Polarity is inverted, the air is being pushed and pulled
  simultaneously, which means that two opposite Phases counter-position
  against each other, creating a so-called Phase Cancellation. An
  alignment of two sounds with 90 degree out of phase effectively halfs
  the Amplitude. An alignment of two sounds with 180 degree out of phase
  effectively results in a complete cancellation.

- **Decibel** at Sound Pressure Level (dB SPL) has known ranges:

  Situation                                  | dB SPL
  ------------------------------------------ | ------
  Near-Total Silence (Threshold of Hearing): | 0
  Breathing:                                 | 10
  Whispering:                                | 15
  Library Room:                              | 45
  Speech/Conversation:                       | 60
  Music:                                     | 80
  Noisy Restaurant:                          | 90
  (Ear Damage Potential):                    | 120
  Jet Engine:                                | 120
  (Threshold of Pain):                       | 140
  Balloon Popping:                           | 157

- **Human Way of Hearing**: as sound pressure increases, more and more
  power is required to create the same perceived(!) increase in
  sound loudness. The Decibel unit accounts for this. Because of this
  logarithmic way of human hearing, the well-known dB SPL ratios for
  sound are:

  Ratio   | dB SPL
  ------- | -------
  1 : 10  | -20
  1 : 2   | -6 (double as quiet)
  1 : 1.5 | -3
  1 : 1   | 0
  1.5 : 1 | +3
  2 : 1   | +6 (double as loud)
  10 : 1  | +20

  The reason simply is the formula `diff = (20 * log_10(2 / (2^16-1)))
  - (20 * log_10(1 / (2^16-1))) = 6.02 dB`. Every time we add 6 dB to a
  signal, we actually double the Amplitude of the signal.

- **Decibel** is 1/10 of a Bel and a power ratio between two values.
  Decibel is a relative, logarithmic unit. Keep in mind that Decibel
  for Power is originally calculated `dB = 10 * log_10(Power-Measured
  / Power-Reference)` while Decibel for Amplitude (of Voltage and
  Sound Pressure -- this context here) is calculated as `dB = 20 *
  log_10(Value-Measured / Value-Reference)`. So, be careful when reading
  about dB calculations in general and applying it in the context of
  audio!

  When dealing with Loundness, the relative units are dB and LU with `1 dB = 1 LU`:

  Unit   | Meaning
  ------ | ----------------------------------------
  dB     | Decibel
  LU     | Loudness Unit

- **Full Scale**: In audio there are multiple absolute units:

  Unit   | Meaning
  ------ | ----------------------------------------
  dB SPL | Decibel relative to Sound Pressure Level
  dB FS  | Decibel relative to Full Scale
  dB TP  | Decibel relative to True Peak
  LUFS   | Loudness Unit relative to Full Scale       (EBU R 128)
  LKFS   | Loudness K-weighted relative to Full Scale (ITU-R BS.1770)
  RMS    | Root Mean Square

  The relation of the absolute units is `db FS ~~ LUFS ~~ LKFS ~~
  RMS`. The subtle differences are how the unit is actually measured
  (LUFS/LKFS is based on a K-weighted calculation, RMS is simple
  average).

  So, LUFS is about the perceived loudness according to the
  [Fletcher Munson curve](https://en.wikipedia.org/wiki/Equal-loudness_contour)
  while RMS is a plain mathematical average loundness. Hence, primarily
  use LUFS when dealing with loudness and RMS only as a rough approximation.

- **LUFS** is usually measured over different time ranges:

  Unit         | Meaning             | Measure Time Range
  ------------ | ------------------- | --------------------------
  LUFS m / ML  | Momentary Loudness  | 400 ms
  LUFS s / STL | Short Term Loudness | 3 s
  LUFS i / IL  | Integrated Loudness | total (entire audio track)

  Hence, the more precise relation between LUFS and RMS is `LUFS m ~~ RMS` as
  RMS usually is measured over a time tange of 300 ms.

- **Loudness, Gain, Volume**: **Loudness** is a subjective measure of how
  intensely our ears perceive the sound (**Human Way of Hearing**, dB
  SPL). **Volume** is a measure of the physical **Amplitude** of the
  sound wave. **Gain** is a scale multiplier (1.0 means no change)
  affecting the sound Amplitude as it is being processed.

- **Loudness Target** differs between organizations:

  Organization                 | Loudness Target
  ---------------------------- | ----------------------
  Spotify Loud:                | -11 LUFS i
  Spotify:                     | -14 LUFS i
  YouTube:                     | -14 LUFS i
  Amazon Music:                | -14 LUFS i
  Tidal:                       | -14 LUFS i
  Deezer:                      | -15 LUFS i
  Pandora:                     | -16 LUFS i
  Apple Music / Apple Podcast: | -16 LUFS i
  Spotify Quiet:               | -23 LUFS i
  EBU R128 S1 (TV):            | -23 LUFS i, -18 LUFS s
  EBU R128 (Cinema, TV):       | -23 LUFS i
  Netflix (Dialog):            | -27 LUFS i

  Hence, in practice a useful loudness target is to follow EBU R128 S1
  and try to reach -18 LUFS s and -23 LUFS i. Also, many mixing engineers
  recommend to not target above the loudness of -12 LUFS s to still
  leave enough "headroom" before the "Maximum True Peak Level" reaches
  the "Audio Clipping" area.

- **Maximum True Peak Level** is the maximum db FS value which should
  never be exceeded in order to not reach the "Audio Clipping" area.
  EBU R128 uses -1 dB FS for the "Maximum True Peak Level".

- **Audio Clipping** is mainly specific to Digital Audio Processing
  (DSP) where 0.0 dB FS is usually the highest possible sample
  peak (because of the usual Fixed Point Value representation), and
  an audio signal peaking higher than that will "clip" and distort.
  Analog audio is a little more complicated than that, but the same
  principle applies.

  As dB FS is measured per sample, a maximum of 0 dB FS in DSP can still
  lead to clipping in analog audio because of "inter-sample peaks".
  Hence, dB TP (Decibel relative to True Peak) is usually used as the
  measured unit for "Maximum True Peak Level" instead of dB FS and hence
  the sound limiting usually is recommended to be at -1.0 dB TP.

  As dBFS is described mathematically as `dBFS = 20 *
  log_10(Sample-Level / Max-Level)`, the maximum dBFS value in 16-bit
  DSP is `20 * log_10(1111 1111 1111 1111 / 1111 1111 1111 1111) =
  log_10(1) = 0`. So, the maximum dBFS value will always be 0 by
  definition, since `log_10(1) = 0`. Similarly, the minimum dBFS value
  in the same DSP is `20 * log_10(0000 0000 0000 0001 / 1111 1111 1111
  1111) = -96.32 dBFS`. For the usual high-fidelity 24-bit DSP scenario,
  the corresponding minimum dBFS value is `20 * log_10(0000 0000 0000
  0000 0000 0001 / 1111 1111 1111 1111 1111 1111) = -144.49 dBFS`.

- **Dynamic Range**: the Decibel between the
  Maximum Peak Level (db FS) and the Minimum Peak Level (db FS).
  Music usually needs a much larger Dynamic Range than Voice.

- **Crest Factor**: or Peak to Short Term Loudness (PSR) is the ratio
  of the **Maximum True Peak Level** and the average loudness (usually
  in LUFS s). The Crest Factor indicates how large the (upper part of
  the) dynamic range is or how extreme the (upper) peaks are. A Crest
  Factor of 1 indicates no peaks at all. Higher Crest Factors indicate
  stronger peaks and hence a wider dynamic range. The art of audio
  mastering is to find a reasonable balance between Crest Factor (wide
  dynamic range) and Loudness. Crest itself is sometimes also the name
  for the plain db FS difference between Maximum True Peak Level and the
  average loudness.

- **Loudness/Volume Scale**: The audio volume full scale can be somewhat
  segmented in 3 dB steps (1.5 louder/quieter) like this and noise and
  voice areas marked on it for a reference for the configuration of
  certain [Audio Parameters](audio-params.md):

    ```txt
    db FS Area                        Noise   Voice Target Reference
    ----- --------------------------- ------- ----- ------ ------------------------
        0 ==== very loud ============                      (-1 dB TP: EBU R128)
     -  3                                     X
     -  6                                     X
     -  9                                     X
     - 12 ==== loud =================         X     X      (-12 LUFS s: Usual Maximum of Mixing Engineers)
     - 15                                     X     X
     - 18                                     X     XX     (-18 LUFS s: EBU R128 S1)
     - 21                                     X     X
     - 24 ==== regular ==============         X     X      (-23 LUFS i: EBU R128 S1)
     - 27                                     X
     - 30                                     X
     - 33                                     X
     - 36 ==== quietly ==============         X
     - 39                                     X
     - 42                                     X
     - 45                                     X
     - 48 ==== very quietly =========         X
     - 51                                     X
     - 54                                     X
     - 57
     - 60 ==== Noise Floor Peaks ==== X
     - 63                             X
     - 66                             X
     - 69                             X
     - 72 ==== Noise Floor Majority = X
     - 75                             X
     - 78                             X
     - 81                             X
     - 84 =========================== X
     - 87                             X
     - 90                             X
     - 93                             X
     - 96 =========================== X
     - 99                             X
     -102                             X
    ```

- **Visualizations**: there are multiple audio visualizations in practice:
   - **Volume Meter** is a usual 1-D audio visualization showing the Volume (dB FS / LUFS).
   - **Frequency Spectrum** is a usual 2-D audio visualization (of equalizers) showing on the
     x-axis the Frequency (Hz) and on the y-axis the Volume (dB FS / LUFS).
     This visualization is called to be in the frequency domain.
   - **Envelope Graph** (german **Hüllkurve**) is a usual 2-D audio visualization (of
     expanders, de-essers, and compressors) showing on the x-axis the time
     (s) and on the y-axis the Volume (dB FS / LUFS) of left (positive) and
     right (negative) channels.
     This visualization is called to be in the time domain.
   - **Spectogram** is a usual heatmap-style, colored, 2-D audio
     visualization (of noise suppressors) showing on the x-axis the time (s), on the y-axis the
     Frequency (Hz), and with the color the Volume (dB FS / LUFS).
     This visualization is called to be in the time domain.
   - **Dynamics Response Graph** is a usual static 2-D audio configuration visualization (of
     gates, expanders, compressors, and limiters) showing
     on the x-axis the incoming signal Volume (dB FS / LUFS) and on
     the y-axis the outgoing signal Volume (dB FS / LUFS).

- **Generated Sound**: audio engineers sometimes use different generated sounds for testing purposes:
   - **White Noise** consists of random amplitudes across the entire
     frequency range and can be compared to a waterfall with water falling
     at different speeds and hitting different surfaces.
   - **Pink Noise** consists of random amplitudes across the entire frequency range where
     the amplitudes of the higher frequences are less strong than the low
     frequences and can be compared of a light to medium rainfall.
   - **Brown Noise** consists of random amplitudes across the low and mid frequency
     range where the amplitudes of the higher frequences are less strong
     than the low frequences, and can be compared to the hard, gentle surf
     that comes with a storm.
   - **Sine Tone** is an amplitude at just a single frequency, and is considered
     the fundamental sound.

