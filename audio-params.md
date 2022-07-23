
Audio Setup
===========

Parameters for Processing
-------------------------

Version 1.0.0 (2022-07-23)

Keepin the [Audio Basics](audio-basics.md) in mind, I usually use the
following base parameters for the usual [Audio Chain](audio-chain.md) filters:

- Noise Suppression:
    - Voice Threshold: -42 dBFS
- Volume Expansion (Soft Gating):
    - Attack Time (to INCREASE gain reduction): 3 ms
    - Hold Time (to keep gain reduction): 50 ms
    - Release Time (to DECREASE gain reduction): 200 ms
    - Threshold: -54 dBFS
    - Knee: 3 dB
    - Ratio: 1:4
    - Makeup Gain (Compensation): 0 dB
- Frequency Equalization:
    - High-Pass Filter (HPF):             50 Hz, 12 dB/Oct
    - (Male) Voice Body/Warmth Boosting: 215 Hz, 0.75 Q, +3.0 dB, 16 ms Attack, 160 ms Release
    - (Male) Voice Nasal Cutting:        900 Hz, 1.75 Q, -9.0 dB, 16 ms Attack, 160 ms Release
    - (Make) Voice Air Boosting:        4000 Hz, 0.75 Q, +6.0 dB, 16 ms Attack, 160 ms Release
    - Low-Pass Filter (LPF):           20000 Hz, 6 dB/Oct
- Volume Compression:
    - Attack Time (to DECREASE gain reduction): 3 ms
    - Hold Time (to keep gain reduction): 50 ms
    - Release Time (to INCREASE gain reduction): 200 ms
    - Threshold: -18 dBFS
    - Knee: 3 dB
    - Ratio: 2:1
    - Makeup Gain (Compensation): +3 dB
- Volume Leveling:
    - Target Loudness: -23 dBFS
- Volume Limiting (Hard Compression):
    - Threshold: -0.5 dB

