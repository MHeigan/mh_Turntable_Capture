# mh_Turntable_Capture v0.5.0

Motion-controlled image capture for edelkrone HeadONE and SliderONE gear on
Windows -- turntable capture, Precision Tuning, keyframed Bezier moves and
HDR panoramas, with every photo saved at the position it was actually taken.

> mh_Turntable_Capture is not made or endorsed by edelkrone, but is an example of what's possible with the edelkrone SDK.

## Features

- **Turntable capture** -- a HeadONE on the Turntable Module turns the object
  through any number of stops per turn; a tilt HeadONE and a SliderONE change
  the camera angle and height between rings. Rings keep turning the same way,
  so the turntable never unwinds.
- **Precision Tuning** -- a short automatic routine learns how your gear
  moves (speed, settling, landing), so every move afterwards is as precise as
  your rig allows.
- **Motion** -- keys captured from the real gear, Bezier curves with ease in
  and out, edited in a graph editor. Play as a timelapse, as stop motion
  (waits for CONTINUE before each photo) or as a real-time move
  (experimental).
- **Panorama and HDRI** -- a spherical grid worked out from your lens and
  overlap, with zenith and nadir; 3 to 9 bracketed exposures per position,
  stepped by the tool or by the camera's own AEB / BKT; PTGui (Papywizard
  XML) and Hugin projects that open with every frame in place.
- **Any camera** -- Nikon and Canon over USB through digiCamControl, or any
  brand through its maker's tethering software (watch folder).
- **Measured** -- an XMP sidecar per photo and a CSV log per session with the
  planned and the measured position.
- **Photogrammetry** -- previewed in its own tab; coming in a feature
  release.
- **Safe by design** -- STOP or Esc halts everything; stall, signal and
  dead-man guards on every move; low-battery checks.
- **Update check** -- Help -> Check for Updates reads this repository's
  releases page.

## Distribution

The release zip holds:

| File | |
|---|---|
| `mh_Turntable_Capture_Win_x64_v0_5_0.exe` | the program -- unzip and double-click |
| `mh_Turntable_Capture_v0_5_0_User_Manual.pdf` | user manual |
| `License_Agreement.pdf`, `License.txt` | licence terms |
| `README.txt` | quick start |
| `THIRD_PARTY_NOTICES.txt` | open-source notices |
| `SHA256SUMS.txt`, `release_manifest.cat`, `manifest.json`, `release_info.txt` | checksums and signed catalogue |
| `_internal\` | runtime files -- do not modify |

No installer, Python or other software is needed.

## System requirements

| Item | Requirement |
|---|---|
| Windows | 10 or 11, 64-bit |
| Bluetooth | Bluetooth LE -- built in, or a USB adapter |
| edelkrone gear | HeadONE (Turntable Module or Tilt Module) and / or SliderONE |
| Camera (optional) | Nikon / Canon over USB via digiCamControl (free), or any brand via its own tethering software |
| Screen | 1920 x 1080 or larger |

## Supported formats

Photos stay in whatever format the camera saves (JPEG, RAW, TIFF). The tool
writes XMP sidecars, CSV session logs, `session.json`, and for panoramas a
Papywizard XML (PTGui) and a Hugin `.pto`.

## Licence

Free software, (C) 2026 Martin P. Heigan, licensed
[CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/legalcode). See [LICENSE.md](LICENSE.md).

edelkrone, HeadONE and SliderONE are trademarks of their owner. digiCamControl, RealityCapture, RealityScan, Agisoft Metashape, COLMAP, PTGui, Hugin, Canon, Nikon and other names are the property of their owners and are used only to describe compatibility.

## Security

The exe is signed with a Certum code signing certificate, RFC 3161 timestamped, and was submitted to Microsoft (WDSI) and VirusTotal
before release. Each release carries `SHA256SUMS.txt` and a signed catalogue
(`release_manifest.cat`).

## Keyboard shortcuts

| Key | Action |
|---|---|
| Esc | STOP -- halts all motion on every unit |

## Safety

The tool moves real equipment. Keep the motion path clear of people and
objects, and know where STOP is before you press START.

## More tools

<https://anti-matter-3d.com/tools/>
