# itty DLNA is a tiny and ultra light weight Universal DLNA Media Server

> **Repurpose an old laptop into a modern DLNA Media Server.**

itty DLNA: tiny, bit-perfect media server for Windows XP and up, able to stream bit perfect high resolution audio to legacy and modern devices.

<img width="1277" height="679" alt="1" src="https://github.com/user-attachments/assets/17a589bb-daf2-4c9b-85fb-377c4c1b46e6" />

<img width="1279" height="681" alt="2" src="https://github.com/user-attachments/assets/1b816f4c-fb24-446d-be30-986702e8d0fe" />

## Easy, small and light

One EXE of about 830 KB, with no installer, no runtimes, no .NET or Java, and no dependencies.

Uses only Windows’ own components and runs from any folder or even an old 1.0 USB stick.

Measured on an Atom N570 netbook with 2 GB RAM, a mechanical hard disk and Win7 x86: about 35 MB of RAM with roughly 20,900 files shared (16,096 tracks, 222 videos, 4,552 photos).
About 5% CPU while streaming on that same low-end Atom.
Base memory is about 5 MB, plus roughly 1.5 KB per file.
Runs on Windows XP SP3 and later, 32- and 64-bit, on any x86 CPU (no SSE needed).
Scanning uses every CPU core but runs at low priority, so it never interrupts playback.

## High Resolution Sound and Picture Quality

Bit-perfect: files are sent untouched, with no transcoding or resampling.
Full hi-res support: 24-bit/192 kHz and above, plus DSD64 to DSD512.

## Supported formats

Audio: FLAC, WAV (including RF64), DSF, DFF (DSD and DST), ALAC, AIFF/AIFC, APE, MP3, AAC (ADTS/M4A/M4B), WMA (including Lossless), OGG (Vorbis, Opus, FLAC).

Video: MP4/M4V, MKV, WEBM, AVI/DivX, MOV/QT, WMV/ASF, MPEG/VOB, TS, M2TS/MTS.

Images: JPEG, PNG, BMP, GIF.

## Compatibility

Standard DLNA / UPnP media server.
Works with smart TVs, Blu-ray and DVD players, VLC, Kodi, phones and tablets (Android and iOS apps), and network streamers such as Yamaha MusicCast, MCR-N670 and WXC-50.
Serves album art (embedded or cover.jpg/folder.jpg).
Lists album tracks in track-number order, multi-disc albums included.
Seeking and resume work with any device that supports them.
Compatibility options for picky devices (FLAC/WAV type settings).

## Features

Share files or whole folders by drag-and-drop.
Watches shared folders and updates automatically.
Handles USB drives and network shares that go offline and come back.
Live “Now streaming” panel showing the device, track, progress and speed.
CPU meter and activity log.
Serve audio, video and images can each be switched off, for faster scans and more privacy.
Optionally Starts with Windows, minimizes to the tray, and shows tray notifications.
Choice of port and network adapter, and a custom server name.
Long file paths and Unicode file names are fully supported.
Settings are stored in a ini file created in the same folder where the program is executed

## Optional Start with Windows

When you tick “Start with Windows”, itty DLNA writes one value to the current user’s part of the registry:

Key: HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run

Value name: itty DLNA
Type: REG_SZ (a text value)
Data: "C:\full\path\to\itty DLNA.exe" /tray. The quotes keep paths with spaces working, and /tray makes it start minimized in the tray.
Unticking deletes that value.
Moved EXE: if the option is on, each launch rewrites the path, so moving the EXE doesn’t break startup.
Per user: it applies to the current user only, needs no admin rights and triggers no UAC prompt.

## What differs between Windows versions

XP, Vista and 7: the same key and value, with nothing else involved.

64-bit Windows: this per-user key is shared between 32- and 64-bit programs. That means it doesn’t get moved to a separate WOW6432Node location the way HKEY_LOCAL_MACHINE entries do, so the 32-bit EXE needs no special handling.

Windows 8, 10 and 11:
Start-up delay: Windows deliberately waits about 10 seconds or more after you sign in before launching programs from this key. The DLNA server just comes online a little later.

Turning startup off outside itty DLNA: 
You can also disable it in Task Manager’s Startup tab or in Settings → Apps → Startup. Windows then leaves the value in place and records its own on/off setting in …\CurrentVersion\Explorer\StartupApproved\Run. That setting is a binary value named itty DLNA, and its first byte is 02 for enabled and 03 for disabled.

If you manually disable it in Task Manager, the “Start with Windows” box in Options still shows as ticked, because the app only checks for its own value.

## Free The short version: 
No fees, No ads, no telemetry and no accounts, just run it and enjoy it!

## You Own It. Forever. Free.
This app is released entirely free of charge, for lifetime of use, no subscriptions, no fees, no expiration, no telemetry, no accounts, you just own it. You have the absolute right to enjoy full, unrestricted use across your environments forever, without a single cent exchanged, and no hidden fees. Optimized for universal compatibility, it has an MIT license, and it bridges generations of technology by supporting everything from Windows XP x86 through Windows 11 x64.

## Features
* **Zero Cost:** 100% free for everyone, no subscrriptions, no fees, no paywalls, no accounts, and no telemetry.
* **Stream Anywhere:** Streams audio, video, and images natively to smart TVs, consoles, and phones.
* **Massive Compatibility:** Lightweight engine running on legacy hardware all the way from Windows XP, Windows Vista, Windows 7, Windows 8, Windows 10, and up to Windows 11 on all x86 / x64 variants.

## 🛑 Project Status & Support
This software is finished, fully functional, and provided purely as-is. 
* **No Tech Support:** I cannot help you configure your home network, routers, or firewalls.
* **No Feature Requests:** The app is very basic and probably will not be receiving updates or new features unless there's  a major performance issue. 
Please enjoy the app exactly as it is!

## Minimum System Requirements

CPU: 
Its coded in C++ for speed and simplicity, the EXE is built for plain Windows x86 with no SSE needed, so anything that runs Windows XP SP3 will start it. An AMD K6-2 or Pentium II processor at about 200–300 MHz should be able to stream audio really well, For high-bitrate video the limits are the disk and network rather than the processor.

- AMD K6-2 300 Mhz
- Intel Pentium II 300 Mhz | Celeron 300A 300 mhz
- Cyrix M-II 300 (233 mhz)


RAM: 
On Windows XP 32 bit roughly 5 MB of base RAM use plus about 1.5 KB per file. That puts a 1,000-track library around 7 MB and 100,000 files around 150 MB RAM.

Minimum OS: Windows XP 32 bit with 128 MB RAM.
Comfortable: Windows XP 32 bit with 256 MB RAM, or 1 GB on Windows7 x86.

Disc: 
Any hard drive is fast enough. Even DSD512, the heaviest audio format, needs only about 5.6 MB/s.

Network: 
100 Mbit wired for hi-res audio and video. 
802.11g Wi-Fi can carry FLAC up to 24/192 and DSD64 with full link speed, but not much above that.

Current Test Systems:
Emachines em355 Atom N570 2GB DDR3 RAM, Windows7 x86 with a media library of 20,900 files = 35 MB RAM, about 5% CPU
Compaq Presario 5BW353 Pentium III 512 MB RAM, WinXP x86 with a media library of 2,938 files = 9 MB RAM, about 7% CPU

## VirusTotal Report & False Positives
2 out of 71 scanners report a risk, namely Arctic Wolf (Unsafe) and CrowdStrike Falcon (Win/malicious_confidence_60% (D)) both are false positives by lazy antivirus apps that just like to flag unknown executable files left and right.

Those two detections are lousy guesses by AI-based scanners, not matches against known malware. Arctic Wolf only says “Unsafe”, and CrowdStrike itself rates it just 60% likely. These scanners tend to flag small, unsigned programs that also open network ports and can optionally add themselves to Windows startup. A media server and itty DLNA does all three for legitimate reasons, so nothing in the code needs to change.

## Troubleshooting
Audio / video skips - Check wireless signal power and actual transmission speeds, on really old g wireless adapters with poor signal quality, larger audio/video files can begin to skip.  
