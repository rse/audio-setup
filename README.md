
Audio Setup
===========

Version 1.0.6 (2022-06-11)

Personal Audio Chain
--------------------

The opinionated audio chain currently used by [Dr. Ralf S. Engelschall](https://engelschall.com) in
his various video streaming setups is based on a [logical audio processing graph](audio-chain.pdf)
(which you can also see again physically in the [Cantabile](audio-chain/screenshot-02-hosting.png) component)
which sits between two speaker output channels and a microphone input channel.
The audio chain in particular is based on the following products:

- **VoiceMeeter Potato** for the [audio track routing](audio-chain/screenshot-01-routing.png)<br/>
  Rationale: simply the most flexible and hardware-independent router/mixer for Windows
- **Cantabile** for the [VST plugin hosting](audio-chain/screenshot-02-hosting.png)<br/>
  Rationale: provides the best ASIO integrated VST host for use with VoiceMeeter Potato
- **BlueCat Dynamics** for voice-over on output [channel 1](audio-chain/screenshot-03-voiceover1.png) and [channel 2](audio-chain/screenshot-04-voiceover2.png)<br/>
  Rationale: simply one of the best and most flexible dynamics processors
- **BlueCat Dynamics** for [side-chain pre-processing](audio-chain/screenshot-05-ducking-pre.png) and [microphone ducking](audio-chain/screenshot-06-ducking.png)<br/>
  Rationale: simply one of the best and most flexible dynamics processors
- **Acon Digital DeVerberate** for [room reverb removal](audio-chain/screenshot-07-de-reverb.png)<br/>
  Rationale: cheaper than DeRoom and as good in quality (also needed because of a condenser mic and 50-100cm distance where a dynamic mic cannot be used)
- **Audionamix Instant Dialogue Cleaner (IDC)** for [noise suppression](audio-chain/screenshot-08-de-noiser.png)<br/>
  Rationale: cheaper than Clarity Vx Pro and better in quality perception
- **Waves Sibilance** for [de-esser](audio-chain/screenshot-09-de-esser.png)<br/>
  Rationale: very good quality
- **TDR Nova GE** for [cutting equalization](audio-chain/screenshot-10-cut-eq.png)<br/>
  Rationale: just a flexible parametric equalizer
- **BlueCat Dynamics** for [expansion](audio-chain/screenshot-11-expander.png)<br/>
  Rationale: simply one of the best and most flexible dynamics processors
- **BlueCat Dynamics** for [compression](audio-chain/screenshot-12-compressor.png)<br/>
  Rationale: simply one of the best and most flexible dynamics processors
- **TDR Nova GE** for [boosting equalization](audio-chain/screenshot-13-boost-eq.png)<br/>
  Rationale: just a flexible parametric equalizer
- **Acon Digital Reverb** for optional [voice reverb addition](audio-chain/screenshot-14-reverb.png)<br/>
  Rationale: just a possible reverb generator
- **TDR Limiter GE** for [volume limiting](audio-chain/screenshot-15-limiter.png)<br/>
  Rationale: a very flexible limiter

For the fine-tuning of the audio-chain, the following additional products are also used:

- **Melda Production MRecorder** for optional [track recording](audio-chain/screenshot-16-recorder.png)<br/>
  Rationale: a sufficient recorder
- **Cantabile Built-In Player** for optional track playing<br/>
  Rationale: a sufficient player
- **YouLean Loudness Meter** for optional [loudness metering](audio-chain/screenshot-17-loudness.png)<br/>
  Rationale: simply the best loudness meter at all
- **Voxengo SPAN Plus** for optional [spectrum visualization](audio-chain/screenshot-18-spectrum.png)<br/>
  Rationale: simply the best spectrum visualizer at all

Products for Audio Chains
-------------------------

This is [Dr. Ralf S. Engelschall](https://engelschall.com)'s
opinionated list of useful software components for setting up a
full-featured Audio processing pipeline under Windows 10/11
(x64). For this, beside the base application, multiple [VST
Plugins](https://en.wikipedia.org/wiki/Virtual_Studio_Technology) and
companion tools should be installed. The intention of this collection is
to easily locate all the essential resources. The list is the result
of setting up various audio chains at home and in the software industry.

### Audio Mixer/Routing

- **VoiceMeeter Potato** 3.0.2.2 ($) [RECOMMENDED]<br/>
  Audio Channel Mixer, Virtual Audio Cable<br/>
  [Homepage](https://vb-audio.com/Voicemeeter/potato.htm)
  [Download](https://download.vb-audio.com/Download_CABLE/Voicemeeter8Setup.exe)

- **Virtual Audio Cable (VAC)** 4.66 ($$) [RECOMMENDED]<br/>
  Virtual Audio Cable<br/>
  [Homepage](https://vac.muzychenko.net/en/)
  [Download](https://software.muzychenko.net/trials/vac466.exe)

### VST Host

- **Cantabile** 4-4047 (0/$$) [RECOMMENDED]<br/>
  VST Host (can link into VoiceMeeter via ASIO inserts)<br/>
  [Homepage](https://www.cantabilesoftware.com/)
  [Download](https://download.cantabilesoftware.com/SetupCantabile-4047.exe)

- **BlueCat PatchWork** 2.52 ($$)<br/>
  VST Host (can act standalone or as a VST plugin itself)<br/>
  [Homepage](https://www.bluecataudio.com/Products/Product_PatchWork/)
  [Download](https://www.bluecataudio.com//Vault/Products/Product_PatchWork/BlueCatPatchWorkVST3Demo-x64Setup.exe)

- **BlueCat MB-7 Mixer** 3.42 ($$)<br/>
  Multi-Band VST Host (acts as a VST plugin itself)<br/>
  [Homepage](https://www.bluecataudio.com/Products/Product_MB7Mixer/)
  [Download](https://www.bluecataudio.com/Products/Product_MB7Mixer/)

- **Audified inTone 2 Solo** 2.5.9 (0)<br/>
  VST Host (can act standalone)<br/>
  [Homepage](https://shop.audified.com/products/intone-2-solo-1)
  [Download](https://shop.audified.com/products/intone-2-solo-1)

- **Audified inTone 2** 2.5.9 ($$)<br/>
  VST Host (can act standalone)<br/>
  [Homepage](https://shop.audified.com/products/intone-2)
  [Download](https://shop.audified.com/products/intone-2)

- **LightHost** 1.2.1 (0)<br/>
  Simple VST Host (acts standalone)<br/>
  [Homepage](https://github.com/rolandoislas/LightHost)
  [Download](https://github.com/rolandoislas/LightHost/releases/download/v1.2.1/Light.Host.1.2.1.Win64.zip)

- **BandLab Cakewalk** 2022.02.1 (0)<br/>
  Digital Audio Workstation (with VST support)<br/>
  [Homepage](https://www.bandlab.com/products/cakewalk)
  [Download](https://downloads.bandlab.com/cakewalk/setup/CakewalkSetup.exe)

- **Cockos Reaper** 6.59 ($$)<br/>
  Digital Audio Workstation (with VST support)<br/>
  [Homepage](https://www.reaper.fm/)
  [Download](https://www.reaper.fm/files/6.x/reaper659_x64-install.exe)

- **OcenAudio** 3.11.12 (0)<br/>
  Audio Editor (with VST support)<br/>
  [Homepage](https://www.ocenaudio.com/)
  [Download](https://www.ocenaudio.com/start_download/ocenaudio64.exe)

- **Audacity** 3.1.3 (0)<br/>
  Audio Editor (with VST support)<br/>
  [Homepage](https://www.audacityteam.org/)
  [Download](https://github.com/audacity/audacity/releases/download/Audacity-3.1.3/audacity-win-3.1.3-x64.exe)

### VST Plugin: Suites/Bundles

- **Reaper ReaPlugs** 2.36 (0)<br/>
  Audio VST Plugin-Suite<br/>
  [Homepage](https://www.reaper.fm/reaplugs/)
  [Download](https://www.reaper.fm/reaplugs/reaplugs236_x64-install.exe)

- **MFreeFXBundle** 15.02 (0/$$)<br/>
  Audio VST Plugin-Suite<br/>
  [Homepage](https://www.meldaproduction.com/MFreeFxBundle)
  [Download](https://www.meldaproduction.com/downloads/down?name=maudioplugins&platform=win&version=15.02&mirror=bunnycdn&url=https%3A%2F%2Fmeldaproduction.b-cdn.net%2Fdownload%2Fmaudioplugins%2Fmaudioplugins_15_02_setup.exe&checksum=e960c04e1f3d1e1b066eee9ca43eddc3ad9ffab0)

- **Blue Cat Freeware Plug-Ins Pack II** 2022-01 (0) [RECOMMENDED]<br/>
  Audio VST Plugin-Suite (FreqAnalyst, Gain, Triple-EQ, etc)<br/>
  [Homepage](https://www.bluecataudio.com/Products/Bundle_FreewarePack/)
  [Download](https://www.bluecataudio.com/Vault/Products/Bundle_FreewarePack/BlueCatFreewarePackVST3-x64Setup.exe)

- **FET Bundle** 5.0/2.0/2.0 (0)<br/>
  Audio VST Plugins (Compressor, Saturator, Transient Enhancer)<br/>
  [Homepage](https://www.patreon.com/posts/51962024)
  [Download](https://analogobsession.com/wp-content/uploads/2021/06/FETISH_5.0.exe)
  [Download](https://analogobsession.com/wp-content/uploads/2021/06/FetDrive_2.0.exe)
  [Download](https://analogobsession.com/wp-content/uploads/2021/06/FetSnap_2.0.exe)

### VST Plugin: All-In-One

- **Speachy** 1.0 ($$) [RECOMMENDED]<br/>
  All-In-One VST Plugin (Compressor, De-Esser, Noise Gate, Noise Suppressor, Equalizer, Limiter)<br/>
  [Homepage](https://www.neverdieaudio.com)
  [Download](https://ccf23558-eb52-443e-bd9b-6383d021f85b.filesusr.com/archives/5f8f59_43f328c2f70043d29795b549ac0810ee.zip?dn=Speachy_1_0_setup_WIN.ZIP)

- **Voxessor** 0 ($$)<br/>
  All-In-One VST Plugin (Compressor, De-Esser, Noise Gate, etc)<br/>
  [Homepage](https://www.waproduction.com/plugins/view/voxessor)
  [Download](https://www.waproduction.com/plugins/view/voxessor)

- **Waves eMo D5 Dynamics** 13.0 ($$)<br/>
  All-In-One VST Plugin (De-Esser, Compressor, Gate, Limiter)<br/>
  [Homepage](https://www.waves.com/plugins/emo-d5-dynamics)
  [Download](https://www.waves.com/plugins/emo-d5-dynamics)

- **Waves Scheps Omni Channel** 13.0 ($$)<br/>
  All-In-One VST Plugin (Compressor, Equalizer, Gate)<br/>
  [Homepage](https://www.waves.com/plugins/scheps-omni-channel)
  [Download](https://www.waves.com/plugins/scheps-omni-channel)

- **Fuse Audio Labs VCS-1** 1.0.1 ($$)<br/>
  All-In-One VST Plugin (Compressor, Expander, Equalizer, Gate)<br/>
  [Homepage](https://fuseaudiolabs.de/#/pages/product?id=301012112)
  [Download](https://fuseaudiolabs.de/vendor/fuseaudiolabs/php/account.php?op=downloadfile&name=fuse_audio_labs_vcs1_win_1_0_1.zip)

- **iZotope Neutron 4** 4 ($$$)<br/>
  All-In-One VST Plugin (Compressor, Expander, Equalizer, Gate, etc)<br/>
  [Homepage](https://www.izotope.com/en/products/neutron.html)
  [Download](https://www.izotope.com/en/products/neutron.html)

### VST Plugin: Reverberation Removal

- **Acon Digital DeVerberate** 3.0.4 ($$) [RECOMMENDED]<br/>
  Audio VST Plugin (Room Reverberation Removal)<br/>
  [Homepage](https://acondigital.de/produkte/deverberate/)
  [Download](https://acondigital.de/produkte/deverberate/)

- **Accentize DeRoom Pro** 2.0.4 ($$$)<br/>
  Audio VST Plugin (Room Reverberation Removal)<br/>
  [Homepage](https://www.accentize.com/deroom-pro/)
  [Download](https://www.accentize.com/deroom-pro/)

- **Accentize DeRoom** 2.0.1 ($$)<br/>
  Audio VST Plugin (Room Reverberation Removal)<br/>
  [Homepage](https://www.accentize.com/deroom/)
  [Download](https://www.accentize.com/deroom/)

### VST Plugin: Noise Suppression (for any non-voice sounds)

- **Waves Clarity Vx Pro** 2022-05 ($$$)<br/>
  Voice Cleaner, separates voice via AI/ML, CPU-heavy<br/>
  [Homepage](https://www.waves.com/plugins/clarity-vx-pro)
  [Download](https://www.waves.com/plugins/clarity-vx-pro)

- **Waves Clarity Vx** 2022-05 ($$)<br/>
  Voice Cleaner, separates voice via AI/ML, CPU-heavy<br/>
  [Homepage](https://www.waves.com/plugins/clarity-vx)
  [Download](https://www.waves.com/plugins/clarity-vx)

- **Accentize VoiceGate** 2.0.8 ($$$) [RECOMMENDED]<br/>
  Voice Cleaner, separates voice via AI/ML<br/>
  [Homepage](https://www.accentize.com/voicegate/)
  [Download](https://www.accentize.com/voicegate/)

- **Audionamix Instant Dialogue Cleaner (IDC)** 2022-05 ($$) [RECOMMENDED]<br/>
  Voice Cleaner, separates voice via AI/ML, has very little latency<br/>
  [Homepage](https://audionamix.com/instant-dialogue-cleaner/)
  [Download](https://audionamix.com/instant-dialogue-cleaner/)

- **Acon Digital Extract Dialog** 1.1.6 ($$)<br/>
  Voice Cleaner, separates voice via AI/ML<br/>
  [Homepage](https://acondigital.de/produkte/extract-dialogue/)
  [Download](https://acondigital.de/produkte/extract-dialogue/)

### VST Plugin: Noise Suppression (for wind/humm/hiss)

- **Waves WNS** 13.0 ($$) [RECOMMENDED]<br/>
  Noise Suppressor, reduces background noise, 6-band attenuation control<br/>
  [Homepage](https://www.waves.com/plugins/ns1-noise-suppressor)
  [Download](https://www.waves.com/plugins/ns1-noise-suppressor)

- **Waves NS1** 13.0 ($$)<br/>
  Noise Suppressor, reduces background noise, single-knob control<br/>
  [Homepage](https://www.waves.com/plugins/ns1-noise-suppressor)
  [Download](https://www.waves.com/plugins/ns1-noise-suppressor)

### VST Plugin: De-Esser

- **Waves Sibilance** 13.0 ($$) [RECOMMENDED]<br/>
  Audio VST Plugin (De-Esser)<br/>
  [Homepage](https://www.waves.com/plugins/sibilance)
  [Download](https://www.waves.com/plugins/sibilance)

- **FabFilter Pro-DS** 1.19 ($$)<br/>
  De-Esser<br/>
  [Homepage](https://www.fabfilter.com/products/pro-ds-de-esser-plug-in)
  [Download](https://www.fabfilter.com/downloads/ffprods119x64.exe)

- **Sleepy-Time Lisp** 1.0 (0)<br/>
  Audio VST Plugin (De-Esser)<br/>
  [Homepage](https://plugins4free.com/plugin/1662/)
  [Download](https://plugins4free.com/get_plug/STDSP_Lisp_x64.zip)

- **Analog Obsession LOADES** 1.0 (0)<br/>
  Audio VST Plugin (De-Esser)<br/>
  [Homepage](https://www.patreon.com/posts/loades-62370686)
  [Download](https://analogobsession.com/wp-content/uploads/2022/02/LOADES_1.0.exe)

### VST Plugin: Equalization

- **TDR Nova GE** 2.1.5 ($$) [RECOMMENDED]<br/>
  Audio VST Plugin (Parallel Dynamic Parametric Equalizer)<br/>
  [Homepage](https://www.tokyodawn.net/tdr-nova-ge/)
  [Download](https://www.tokyodawn.net/labs/NovaGE/2.1.5/TDR%20Nova%20GE%20Demo%20(installer).zip?x24775)

- **TDR Nova** 2.1.5 (0)<br/>
  Audio VST Plugin (Parallel Dynamic Parametric Equalizer)<br/>
  [Homepage](https://www.tokyodawn.net/tdr-nova/)
  [Download](https://www.tokyodawn.net/labs/Nova/2.1.5/TDR%20Nova%20(installer).zip?x24775)

- **TDR SlickEQ GE** 1.3.7 ($$) [RECOMMENDED]<br/>
  Audio VST Plugin (Parametric Equalizer)<br/>
  [Homepage](https://www.tokyodawn.net/tdr-vos-slickeq-ge/)
  [Download](https://www.tokyodawn.net/labs/SlickEQGE/1.3.7/TDR%20VOS%20SlickEQ%20GE%20Demo%20(installer).zip?x24775)

- **TDR SlickEQ** 1.3.7 (0)<br/>
  Audio VST Plugin (Parameteric Equalizer)<br/>
  [Homepage](https://www.tokyodawn.net/tdr-vos-slickeq/)
  [Download](https://www.tokyodawn.net/labs/SlickEQ/1.3.7/TDR%20VOS%20SlickEQ%20(installer).zip?x24775)

- **Waves F6** 13 ($$)<br/>
  Audio VST Plugin (Parametric Equalizer, Zero Latency)<br/>
  [Homepage](https://www.waves.com/plugins/f6-floating-band-dynamic-eq)
  [Download](https://www.waves.com/plugins/f6-floating-band-dynamic-eq)

- **Waves Q10** 13 ($$)<br/>
  Audio VST Plugin (Parametric Equalizer, Zero Latency)<br/>
  [Homepage](https://www.waves.com/plugins/f6-floating-band-dynamic-eq)
  [Download](https://www.waves.com/plugins/f6-floating-band-dynamic-eq)

- **FabFilter Pro-Q 3** 3.21 ($$$)<br/>
  Audio VST Plugin (Parametric Equalizer, Zero Latency)<br/>
  [Homepage](https://www.fabfilter.com/products/pro-q-3-equalizer-plug-in)
  [Download](https://www.fabfilter.com/downloads/ffproq321x64.exe)

- **Eventide SplitEQ** 1.0.12 ($$)<br/>
  Audio VST Plugin (Parameteric Equalizer, seperate tonal and transient, 80ms Latency)<br/>
  [Homepage](https://www.eventideaudio.com/plug-ins/spliteq/)
  [Download](https://www.eventideaudio.com/downloads/spliteq-installer-win-64-bit)

- **Sonible smart:EQ 3** 3 ($$$)<br/>
  Audio VST Plugin (Parametric Equalizer)<br/>
  [Homepage](https://www.sonible.com/smarteq3/)
  [Download](https://www.sonible.com/smarteq3/)

- **Voxengo Marvel GEQ** 1.11 (0)<br/>
  Audio VST Plugin (Graphical Equalizer)<br/>
  [Homepage](https://www.voxengo.com/product/marvelgeq/)
  [Download](https://www.voxengo.com/files/VoxengoMarvelGEQ_111_Win32_64_VST_VST3_AAX_setup.exe)

### VST Plugins: Ducking

- **Wavesfactory Trackspacer** 2.5.9 ($$)<br/>
  Dynamic 32-Band Sidechain-Based Inverse-Equalizer (for ducking)<br/>
  [Homepage](https://www.wavesfactory.com/audio-plugins/trackspacer/)
  [Download](https://trackspacer-wavesfactory.s3.amazonaws.com/Trackspacer%202.5.9.exe)

- **Audified SpeakUp** 1.0.0 ($)<br/>
  Audio-Ducking: Volume Reduction for Speaking over Audio<br/>
  [Homepage](https://shop.audified.com/products/speakup)
  [Download](https://shop.audified.com/products/speakup)

- **Auto-Duck** 3.0.0-RC4.1 ($)<br/>
  Audio-Ducking: Volume Reduction for Speaking over Audio<br/>
  [Homepage](https://auto-duck.com/)
  [Download](https://auto-duck.com/download-last)

### VST Plugin: Compression

- **BlueCat Dynamics** ($$) [RECOMMENDED]<br/>
  Compressor/Expander<br/>
  [Homepage](https://www.bluecataudio.com/Products/Product_Dynamics/)
  [Download](https://www.bluecataudio.com/Vault/Products/Product_Dynamics/BlueCatDynamicsVST3Demo-x64Setup.exe)

- **TDR Kotelnikov** 1.6.4 (0)<br/>
  Audio VST Plugin (Wideband Dynamic Processor / Compressor)<br/>
  [Homepage](https://www.tokyodawn.net/tdr-kotelnikov/)
  [Download](https://www.tokyodawn.net/labs/Kotelnikov/1.6.4/TDR%20Kotelnikov%20(installer).zip?x24775)

- **TDR Kotelnikov GE** 1.6.4 (0)<br/>
  Audio VST Plugin (Wideband Dynamic Processor / Compressor)<br/>
  [Homepage](https://www.tokyodawn.net/tdr-kotelnikov-ge/)
  [Download](https://www.tokyodawn.net/labs/KotelnikovGE/1.6.4/TDR%20Kotelnikov%20GE%20Demo%20(installer).zip?x24775)

- **FabFilter Pro-C 2** 2.15 ($$$)<br/>
  Compressor<br/>
  [Homepage](https://www.fabfilter.com/products/pro-c-2-compressor-plug-in)
  [Download](https://www.fabfilter.com/downloads/ffproc215x64.exe)

### VST Plugin: Expansion/Gating

- **BlueCat Dynamics** ($$) [RECOMMENDED]<br/>
  Compressor/Expander<br/>
  [Homepage](https://www.bluecataudio.com/Products/Product_Dynamics/)
  [Download](https://www.bluecataudio.com/Vault/Products/Product_Dynamics/BlueCatDynamicsVST3Demo-x64Setup.exe)

- **FabFilter Pro-G** 2.15 ($$$)<br/>
  Expander<br/>
  [Homepage](https://www.fabfilter.com/products/pro-g-gate-expander-plug-in)
  [Download](https://www.fabfilter.com/downloads/ffprog129x64.exe)

- **Rob Perry Gate** 1.3.0 (0)<br/>
  Audio VST Plugin (Sidechain Noise-Gate)<br/>
  [Homepage](https://plugins4free.com/plugin/2213/)
  [Download](https://plugins4free.com/get_plug/BPAGate_x64.zip)

### VST Plugin: Saturation

- **Slate Digital Fresh Air** 1.0.8 (0)<br/>
  Audio VST Plugin (dynamic high frequency processor)<br/>
  [Homepage](https://slatedigital.com/fresh-air/)
  [Download](https://slatedigital.com/fresh-air/)

### VST Plugin: Volume Limiting

- **TDR Limiter GE 6** 1.2.4 ($$) [RECOMMENDED]<br/>
  Audio VST Plugin<br/>
  [Homepage](https://www.tokyodawn.net/tdr-limiter6-ge/)
  [Download](https://www.tokyodawn.net/labs/Limiter6GE/1.2.4/TDR%20Limiter%206%20GE%20Demo%20(installer).zip?x24775)

- **TDR VladG Limiter No6** (0)<br/>
  Audio VST Plugin (predecessor to TDR Limiter?)<br/>
  [Homepage](https://www.tokyodawn.net/vladg-limiter-n6/)
  [Download](https://www.tokyodawn.net/labs/vladgsound/Limiter6-v102b.zip?x24775)

### VST Plugin: Volume Leveling

- **Waves Playlist Rider** 2022-05 ($$)<br/>
  Audio VST Plugin (Microphone Volume Balancer)<br/>
  [Homepage](https://www.waves.com/plugins/playlist-rider)
  [Download](https://www.waves.com/plugins/playlist-rider)

- **Waves Vocal Rider** 2022-05 ($$)<br/>
  Audio VST Plugin (Microphone Volume Balancer)<br/>
  [Homepage](https://www.waves.com/plugins/vocal-rider)
  [Download](https://www.waves.com/plugins/vocal-rider)

- **DynaRide 2** 2 ($$)<br/>
  Audio VST Plugin (Volume Balancer)<br/>
  [Homepage](https://www.tbproaudio.de/products/dynaride)
  [Download](https://www.tbproaudio.de/products/dynaride)

### VST Plugin: Microphone Auto-Mixing

- **WTAutomixer** V2 ($$$) [RECOMMENDED]<br/>
  Audio VST Plugin (Microphone Volume Balancer)<br/>
  [Homepage](https://www.wtautomixer.com/)
  [Download](https://releases.wavetoolapi.com/wtam/WTAutomixer-setup.zip)

- **Junger Audio-Level Magic** 2022-05 ($$$)<br/>
  Audio VST Plugin (Microphone Volume Balancer)<br/>
  [Homepage](https://www.flux.audio/project/junger-audio-level-magic/)
  [Download](https://www.flux.audio/project/junger-audio-level-magic/)

- **TBProAudio AMM2** 2.0.15 ($$)<br/>
  Audio VST Plugin (Microphone Volume Balancer)<br/>
  [Homepage](https://www.tbproaudio.de/products/amm)
  [Download](https://www.tbproaudio.de/assets/content/download/AMM2_Installer_WIN_2015.zip)

### VST Plugin: Volume Metering

- **Youlean Loudness Meter** 2.4.3 ($$) [RECOMMENDED]<br/>
  Audio VST Plugin (Volume Meter)<br/>
  [Homepage](https://youlean.co/youlean-loudness-meter/)
  [Download](https://youlean-129cf.kxcdn.com/wp-content/uploads/2021/02/Youlean-Loudness-Meter-2-V2.4.3-Windows-2.zip)

- **TBProAudio mvMeter2** 2.4.2 (0)<br/>
  Audio VST Plugin (Volume Meter)<br/>
  [Homepage](https://www.tbproaudio.de/products/mvmeter2)
  [Download](https://www.tbproaudio.de/assets/content/download/mvMeter2nogpu_Installer_WIN_242.zip)

- **TBProAudio dpMeter5** 5.2.2 (0)<br/>
  Audio VST Plugin (Volume Meter)<br/>
  [Homepage](https://www.tbproaudio.de/products/dpmeter)
  [Download](https://www.tbproaudio.de/assets/content/download/dpMeter5nogpu_Installer_WIN_522.zip)

- **Waves Plus Loudness Meter (WLM)** 13.0 ($$)<br/>
  Audio VST Plugin (Volume Meter)<br/>
  [Homepage](https://www.waves.com/plugins/wlm-loudness-meter)
  [Download](https://www.waves.com/plugins/wlm-loudness-meter)

### VST Plugin: Spectrum Visualization

- **Voxengo SPAN Plus** 3.14 ($$) [RECOMMENDED]<br/>
  Audio VST Plugin (Spectrum Visualizer)<br/>
  [Homepage](https://www.voxengo.com/product/spanplus/)
  [Download](https://www.voxengo.com/files/VoxengoSPANPlus_118_Win32_64_VST_VST3_AAX_setup.exe)

- **Voxengo SPAN** 3.14 (0) [RECOMMENDED]<br/>
  Audio VST Plugin (Spectrum Visualizer)<br/>
  [Homepage](https://www.voxengo.com/product/span/)
  [Download](https://www.voxengo.com/files/VoxengoSPAN_314_Win32_64_VST_VST3_AAX_setup.exe)

### VST Plugin: Channel Panning

- **TBProAudio ST1** 2.0.11 ($)<br/>
  Audio VST Plugin (Volume Meter)<br/>
  [Homepage](https://www.tbproaudio.de/products/st1)
  [Download](https://www.tbproaudio.de/assets/content/download/ST1V2_Installer_WIN_2011.zip)

### VST Plugin: Playing/Recording

- **Voxengo Recorder** 2.20 (0)<br/>
  Audio VST Plugin (WAV-Recorder)<br/>
  [Homepage](https://www.voxengo.com/product/recorder/)
  [Download](https://www.voxengo.com/files/VoxengoVoxformer_220_Win32_64_VST_VST3_AAX_setup.exe)

- **One Small Clue: Grace** 1.0.4.9 (0)<br/>
  Audio VST Plugin (Sampler/Player)<br/>
  [Homepage](https://www.onesmallclue.com/index.html)
  [Download](https://osc.sfo2.digitaloceanspaces.com/Setup_Grace_64bit_Full_1-0-4-9_Windows.exe)

### VST Plugin: Sender/Receiver

- **BlueCat Connector** ($$)<br/>
  Sender/Receiver<br/>
  [Homepage](https://www.bluecataudio.com/Products/Product_Connector/)
  [Download](https://www.bluecataudio.com//Vault/Products/Product_Connector/BlueCatConnectorVST3Demo-x64Setup.exe)

- **SonoBus** (0)<br/>
  High-Quality Network Audio Streaming (Conference Mode)<br/>
  [Homepage](https://www.sonobus.net/)
  [Download](https://www.sonobus.net/releases/sonobus-1.5.1-win.exe)

### Companion Tools

- **OBS Audio Sync** 2019 (0)<br/>
  Audio/Video Synchronization Tool (Video-Based)<br/>
  [Homepage](http://obsaudiosync.com/)
  [Download](https://share.hsforms.com/1GRBSRUxoTSCz56pblQR-WA8z4i)

- **LoistoSYNC** 2021-05 (0)<br/>
  Audio/Video Synchronization Tool (Browser-Source-Based)<br/>
  [Homepage](https://github.com/reaby/loistoSYNC)
  [Download](http://reaby.kapsi.fi/dev/loistosync/)

- **Voice Attack** 1.8.9 (0)<br/>
  Voice Control Commands<br/>
  [Homepage](https://voiceattack.com/)
  [Download](https://voiceattack.com/FileSend.aspx?id=VoiceAttackInstaller64.exe)

- **LoopMIDI** 1.0.16.27 (0)<br/>
  Virtual MIDI Port<br/>
  [Homepage](https://www.tobias-erichsen.de/software/loopmidi.html)
  [Download](http://www.tobias-erichsen.de/wp-content/uploads/2020/01/loopMIDISetup_1_0_16_27.zip)

