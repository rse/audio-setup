
Audio Setup
===========

Personal Audio Chain
--------------------

Version 1.1.6 (2022-07-20)

The opinionated real-time audio chain currently used by [Dr. Ralf S. Engelschall](https://engelschall.com) in
his various real-time video streaming setups is based on a [logical audio processing graph](audio-chain.pdf)
(which you can also see again physically in the [Cantabile](audio-chain/screenshot-02-hosting.png) component)
which sits between two speaker output channels and a microphone input channel.

### Hosting

For hosting the audio chain, the following particular products are used:

- **VoiceMeeter Potato** for the [audio track routing](audio-chain/screenshot-01-routing.png)<br/>
  Rationale: simply the most flexible and hardware-independent router/mixer for Windows
- **Cantabile** for the [VST plugin hosting](audio-chain/screenshot-02-hosting.png)<br/>
  Rationale: provides the best ASIO-integrated VST host for use with VoiceMeeter Potato

### Ducking

For microphone ducking and voice-over, the following pre-processing products are used:

- **BlueCat Dynamics** for voice-over on output [channel 1](audio-chain/screenshot-03-voiceover1.png) and [channel 2](audio-chain/screenshot-04-voiceover2.png)<br/>
  Rationale: simply one of the best and most flexible dynamics processors
- **BlueCat Dynamics** for [side-chain pre-processing](audio-chain/screenshot-05-ducking-pre.png) and [microphone ducking](audio-chain/screenshot-06-ducking.png)<br/>
  Rationale: simply one of the best and most flexible dynamics processors

### Processing

For the primary audio processing chain, the following products are used:

- **Acon Digital DeVerberate** for [room reverb removal](audio-chain/screenshot-07-de-reverb.png)<br/>
  Rationale: zero latency, cheaper and as good in quality as DeRoom
- **Waves WNS** for [noise suppression (phase 1)](audio-chain/screenshot-08-de-noiser-1.png)<br/>
  Rationale: zero latency, no noticable voice distortions, works good as a pre-suppressor
- **Waves NS1** for [noise suppression (phase 2)](audio-chain/screenshot-09-de-noiser-2.png)<br/>
  Rationale: zero latency, no noticable voice distortions, works good on a post-suppressor
- **BlueCat Dynamics** for [expansion](audio-chain/screenshot-10-expander.png)<br/>
  Rationale: simply one of the best and most flexible dynamics processors
- **Waves Sibilance** for [de-essing](audio-chain/screenshot-11-de-esser.png)<br/>
  Rationale: very good quality and no noticable audio distortions
- **Waves F6** for [equalization](audio-chain/screenshot-12-equalizer.png)<br/>
  Rationale: zero latency and flexible enough for a cut-equalization step
- **Slate Digital Fresh Air** for [exciter](audio-chain/screenshot-13-exciter.png)<br/>
  Rationale: zero latency and good results (for a boost-equalization-like processor)
- **Acon Digital Reverb** for optional [voice reverb addition](audio-chain/screenshot-14-reverb.png)<br/>
  Rationale: just a possible reverb generator
- **BlueCat Dynamics** for [compression](audio-chain/screenshot-15-compressor.png)<br/>
  Rationale: simply one of the best and most flexible dynamics processors
- **TDR Limiter GE** for [volume limiting](audio-chain/screenshot-16-limiter.png)<br/>
  Rationale: a very flexible and powerful limiter, near zero latency

### Monitoring

For the fine-tuning of the processing chain, the following additional products are also used:

- **Melda Production MRecorder** for optional [track recording](audio-chain/screenshot-17-recorder.png)<br/>
  Rationale: a sufficient recorder
- **Cantabile Built-In Player** for optional track playing<br/>
  Rationale: a sufficient player
- **YouLean Loudness Meter** for optional [loudness metering](audio-chain/screenshot-18-loudness.png)<br/>
  Rationale: simply the best loudness meter at all
- **Voxengo SPAN Plus** for optional [spectrum visualization](audio-chain/screenshot-19-spectrum.png)<br/>
  Rationale: simply the best spectrum visualizer at all
- **iZotope Insight 2** for optional [spectrogram visualization](audio-chain/screenshot-20-spectogram.png)<br/>
  Rationale: shows a useful spectrogram, especially handy for noise suppression comparison
