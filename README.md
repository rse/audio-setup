
Audio Setup
===========

Version 1.0.1 (2022-06-04)

This is [Dr. Ralf S. Engelschall](https://engelschall.com)'s
opinionated list of software components for setting up a
full-featured Audio processing pipeline under Windows 10/11
(x64). For this, beside the base application, multiple [VST
Plugins](https://en.wikipedia.org/wiki/Virtual_Studio_Technology) and
companion tools should be installed. The intention of this collection is
to easily locate all the essential resources.

The audio processing chain currently used by Dr. Ralf S. Engelschall in particular is based on:
*VoiceMeeter Potato* for the [audio track routing](audio-chain/screenshot-01-routing.png);
*Cantabile* for the [VST plugin hosting](audio-chain/screenshot-02-hosting);
*BlueCat Dynamics* for voice-over on output [channel 1](audio-chain/screenshot-03-voiceover1.png) and [channel 2](audio-chain/screenshot-04-voiceover2.png);
*BlueCat Dynamics* for [side-chain processing](audio-chain/screenshot-05-ducking-pre.png) and [microphone ducking](audio-chain/screenshot-06-ducking.png);
*Acon Digital DeVerberate* for [room reverb removal](audio-chain/screenshot-07-de-reverb.png);
*Audionamix Instant Dialogue Cleaner (IDC)* for [noise suppression](audio-chain/screenshot-08-de-noise.png);
*Waves Sibilance* for [de-esser](audio-chain/screenshot-09-de-esser.png);
*TDR Nova GE* for [cutting equalization](audio-chain/screenshot-10-cut-eq.png);
*BlueCat Dynamics* for [expansion](audio-chain/screenshot-11-expander.png);
*BlueCat Dynamics* for [compression](audio-chain/screenshot-12-compressor.png);
*TDR Nova GE* for [boosting equalization](audio-chain/screenshot-13-boost-eq.png);
*Acon Digital Reverb* for optional [voice reverb addition](audio-chain/screenshot-14-reverb.png);
*TDR Limiter GE* for [volume limiting](audio-chain/screenshot-15-limiter.png);
*Melda Production MRecorder* for optional [track recording](audio-chain/screenshot-16-recorder.png);
*YouLean Loudness Meter* for optional [loudness metering](audio-chain/screenshot-17-loudness.png); and
*Voxengo SPAN Plus* for optional [spectrum visualization](audio-chain/screenshot-18-spectrum.png).

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

- **BlueCat PatchWork** ($$)<br/>
  VST Host (can act standalone or as a VST plugin itself)<br/>
  [Homepage](https://www.bluecataudio.com/Products/Product_PatchWork/)
  [Download](https://www.bluecataudio.com//Vault/Products/Product_PatchWork/BlueCatPatchWorkVST3Demo-x64Setup.exe)

- **LightHost** 1.2.1 (0)<br/>
  Simple VST Host (acts standalone)<br/>
  [Homepage](https://github.com/rolandoislas/LightHost)
  [Download](https://github.com/rolandoislas/LightHost/releases/download/v1.2.1/Light.Host.1.2.1.Win64.zip)

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

- **Waves eMo D5 Dynamics** 2022-05 ($$)<br/>
  All-In-One VST Plugin (De-Esser, Compressor, Gate, Limiter)<br/>
  [Homepage](https://www.waves.com/plugins/emo-d5-dynamics)
  [Download](https://www.waves.com/plugins/emo-d5-dynamics)

- **Waves Scheps Omni Channel** 2022-05 ($$)<br/>
  All-In-One (VST Plugin (Compressor, Equalizer, Gate)<br/>
  [Homepage](https://www.waves.com/plugins/scheps-omni-channel)
  [Download](https://www.waves.com/plugins/scheps-omni-channel)

### VST Plugin: Reverberation Removal

- **Acon Digital DeVerberate** 3.0.4 ($$) [RECOMMENDED]<br/>
  Audio VST Plugin (Room Reverberation Removal)<br/>
  [Homepage](https://acondigital.de/produkte/deverberate/)
  [Download](https://acondigital.de/produkte/deverberate/)

- **Accentize DeRoom Pro** 2022-05 ($$$)<br/>
  Audio VST Plugin (Room Reverberation Removal)<br/>
  [Homepage](https://www.accentize.com/deroom-pro/)
  [Download](https://www.accentize.com/deroom-pro/)

- **Accentize DeRoom** 2022-05 ($$)<br/>
  Audio VST Plugin (Room Reverberation Removal)<br/>
  [Homepage](https://www.accentize.com/deroom/)
  [Download](https://www.accentize.com/deroom/)

### VST Plugin: Noise Suppression

- **Audionamix Instant Dialogue Cleaner (IDC)** 2022-05 ($$) [RECOMMENDED]<br/>
  Audio VST Plugin (Noise Suppressor)<br/>
  [Homepage](https://audionamix.com/instant-dialogue-cleaner/)
  [Download](https://audionamix.com/instant-dialogue-cleaner/)

- **Waves Clarity Vx Pro** 2022-05 ($$$)<br/>
  Audio VST Plugin (Noise Suppressor)<br/>
  [Homepage](https://www.waves.com/plugins/clarity-vx-pro)
  [Download](https://www.waves.com/plugins/clarity-vx-pro)

- **Waves Clarity Vx** 2022-05 ($$)<br/>
  Audio VST Plugin (Noise Suppressor)<br/>
  [Homepage](https://www.waves.com/plugins/clarity-vx)
  [Download](https://www.waves.com/plugins/clarity-vx)

- **Waves NS1** 2022-05 ($$)<br/>
  Audio VST Plugin (Noise Suppressor)<br/>
  [Homepage](https://www.waves.com/plugins/ns1-noise-suppressor)
  [Download](https://www.waves.com/plugins/ns1-noise-suppressor)

- **Waves WMS** 2022-05 ($$)<br/>
  Audio VST Plugin (Noise Suppressor)<br/>
  [Homepage](https://www.waves.com/plugins/ns1-noise-suppressor)
  [Download](https://www.waves.com/plugins/ns1-noise-suppressor)

### VST Plugin: De-Esser

- **Waves Sibilance** 2022-05 ($$) [RECOMMENDED]<br/>
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

- **FabFilter Pro-Q 3** ($$$)<br/>
  Audio VST Plugin (Graphical Equalizer)<br/>
  [Homepage](https://www.fabfilter.com/products/pro-q-3-equalizer-plug-in)
  [Download](https://www.fabfilter.com/downloads/ffproq321x64.exe)

- **Voxengo Marvel GEQ** 1.11 (0)<br/>
  Audio VST Plugin (Graphical Equalizer)<br/>
  [Homepage](https://www.voxengo.com/product/marvelgeq/)
  [Download](https://www.voxengo.com/files/VoxengoMarvelGEQ_111_Win32_64_VST_VST3_AAX_setup.exe)

### VST Plugin: Compression

- **BlueCat Dynamics** ($$) [RECOMMENDED]<br/>
  Compressor/Expander<br/>
  [Homepage](https://www.bluecataudio.com/Products/Product_Dynamics/)
  [Download](https://www.bluecataudio.com/Vault/Products/Product_Dynamics/BlueCatDynamicsVST3Demo-x64Setup.exe)

- **TDR Kotelnikov** 1.6.4 (0)<br/>
  Audio VST Plugin (Wideband Dynamic Processor / Compressor)<br/>
  [Homepage](https://www.tokyodawn.net/tdr-kotelnikov/)
  [Download](https://www.tokyodawn.net/labs/Kotelnikov/1.6.4/TDR%20Kotelnikov%20(installer).zip?x24775)

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

- **WTAutomixer** V2 ($$$) [RECOMMENDED]<br/>
  Audio VST Plugin (Microphone Volume Balancer)<br/>
  [Homepage](https://www.wtautomixer.com/)
  [Download](https://releases.wavetoolapi.com/wtam/WTAutomixer-setup.zip)

- **Junger Audio-Level Magic** 2022-05 ($$$)<br/>
  Audio VST Plugin (Microphone Volume Balancer)<br/>
  [Homepage](https://www.flux.audio/project/junger-audio-level-magic/)
  [Download](https://www.flux.audio/project/junger-audio-level-magic/)

- **Waves Playlist Rider** 2022-05 ($$)<br/>
  Audio VST Plugin (Microphone Volume Balancer)<br/>
  [Homepage](https://www.waves.com/plugins/playlist-rider)
  [Download](https://www.waves.com/plugins/playlist-rider)

- **Waves Vocal Rider** 2022-05 ($$)<br/>
  Audio VST Plugin (Microphone Volume Balancer)<br/>
  [Homepage](https://www.waves.com/plugins/vocal-rider)
  [Download](https://www.waves.com/plugins/vocal-rider)

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

### VST Plugin: Spectrum Visualization

- **Voxengo SPAN Plus** 3.14 ($$) [RECOMMENDED]<br/>
  Audio VST Plugin (Spectrum Visualizer)<br/>
  [Homepage](https://www.voxengo.com/product/spanplus/)
  [Download](https://www.voxengo.com/files/VoxengoSPANPlus_118_Win32_64_VST_VST3_AAX_setup.exe)

- **Voxengo SPAN** 3.14 (0) [RECOMMENDED]<br/>
  Audio VST Plugin (Spectrum Visualizer)<br/>
  [Homepage](https://www.voxengo.com/product/span/)
  [Download](https://www.voxengo.com/files/VoxengoSPAN_314_Win32_64_VST_VST3_AAX_setup.exe)

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

- **Auto-Duck** 3.0.0-RC4.1 ($)<br/>
  Audio-Ducking: Volume Reduction for Speaking over Audio<br/>
  [Homepage](https://auto-duck.com/)
  [Download](https://auto-duck.com/download-last)

- **SonoBus** (0)<br/>
  High-Quality Network Audio Streaming (Conference Mode)<br/>
  [Homepage](https://www.sonobus.net/)
  [Download](https://www.sonobus.net/releases/sonobus-1.5.1-win.exe)

