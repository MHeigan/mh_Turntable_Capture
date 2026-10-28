# mh_Turntable_Capture v1.0.0

Motion-controlled image capture for edelkrone HeadONE and SliderONE gear on
Windows -- turntable capture, photogrammetry, keyframed Bezier moves and HDR
panoramas, with every photo saved at the position it was actually taken.

> mh_Turntable_Capture is not made or endorsed by edelkrone, but is an example
> of what's possible with the edelkrone SDK.

## Features

- **Turntable capture** \-- a HeadONE on the Turntable Module turns the object
  through any number of stops per turn; a tilt HeadONE and a SliderONE change
  the camera angle and height between rings. Rings can alternate direction, and
  a stopped capture can be resumed.
- **Photogrammetry** \-- turns a turntable capture into a project for
  RealityCapture / RealityScan, Agisoft Metashape or COLMAP, with every camera
  already placed, upright and close to real scale. An optional backlit pass
  makes clean masks that keep only the object, and a one-page HTML spin viewer
  shares the result. A Quick Start explains how it works, and PLAN A CAPTURE
  sets up the capture for you.
- **Linked rig** \-- the pan head, slider and tilt head linked as one rig, as
  PAIR does in the edelkrone phone app: every move starts and ends together.
- **Motion** \-- keys captured from the real gear, Bezier curves with ease in and
  out, edited in a graph editor. Play as a timelapse, a continuous timelapse,
  stop motion (waits for CONTINUE before each photo) or one smooth real-time
  move for video, with PREVIEW MOVE and STRETCH.
- **Panorama and HDRI** \-- a spherical grid worked out from your lens
  (rectilinear or fisheye), sensor and overlap, with zenith and nadir; 3 to 9
  bracketed exposures per position, stepped by the tool or by the camera's own
  AEB / BKT; PTGui (Papywizard XML) and Hugin projects that open with every
  frame in place.
- **Tilt limits** \-- set once by hand with the real lens and cable; every tilt
  move on every tab stays inside them, and the tilt reads as camera pitch (+
  up, - down).
- **Precision Tuning** \-- a short automatic routine learns how your gear moves,
  so every move afterwards is as precise as your rig allows.
- **Manual control** \-- joysticks with axis lock, live position readouts, MOVE
  BY / MOVE TO, and the six stored positions (P1-P6) shared with the phone app.
- **Any camera** \-- Nikon and Canon over USB through digiCamControl, or any
  brand through its maker's tethering software (watch folder).
- **Measured** \-- an XMP sidecar per photo and a CSV log per session with the
  planned and the measured position, including the camera pitch.
- **Safe by design** \-- STOP or Esc halts everything; stall, signal and dead-man
  guards on every move; tilt limits and slider ends respected; low-battery
  checks.
- **Update check** \-- Help -> Check for Updates reads this repository's releases
  page.

## Distribution

The release zip holds:


|File                                                                 |                                     |
|---------------------------------------------------------------------|-------------------------------------|
|`mh_Turntable_Capture_Win_x64_v1_0_0.exe`                            |the program -- unzip and double-click|
|`mh_Turntable_Capture_v1_0_0_User_Manual.pdf`                        |user manual                          |
|`License_Agreement.pdf`, `License.txt`                               |licence terms                        |
|`README.txt`                                                         |quick start                          |
|`THIRD_PARTY_NOTICES.txt`                                            |open-source notices                  |
|`SHA256SUMS.txt`, `release_manifest.cat`, `manifest.json`, `release_info.txt`|checksums and signed catalogue       |
|`_internal\\`                                                        |runtime files -- do not modify       |

No installer, Python or other software is needed.

## Quick start

1.  Unzip anywhere and double-click the exe. Close the edelkrone phone app
    first (or switch the phone's Bluetooth off).
2.  **CONTROL** tab: tick the units you want and press **CONNECT**. On a HeadONE
    card set *Use as* to Turntable, Pan or Tilt.
3.  With a tilt head, set the **tilt limits** (LIMITS... in the TILT row).
4.  **PRECISION TUNING** tab: **TUNE MY GEAR** (recommended, once per set-up).
5.  **CAPTURE**, **MOTION** or **PANORAMA**: set up and press **START**. For
    photogrammetry, start from **PLAN A CAPTURE** on the **PHOTOGRAMMETRY** tab.

## System requirements


|Item             |Requirement                                                                                  |
|-----------------|---------------------------------------------------------------------------------------------|
|Windows          |10 or 11, 64-bit                                                                             |
|Bluetooth        |Bluetooth LE -- built in, or a USB adapter                                                   |
|edelkrone gear   |HeadONE (Turntable Module or Tilt Module) and / or SliderONE                                 |
|Camera (optional)|Nikon / Canon over USB via digiCamControl (free), or any brand via its own tethering software|
|Screen           |1920 x 1080 or larger                                                                        |

## Supported formats

Photos stay in whatever format the camera saves (JPEG, RAW, TIFF); for
photogrammetry, developed images are matched to the capture by file name. The
tool writes XMP sidecars, CSV session logs and `session.json`; for panoramas a
Papywizard XML (PTGui) and a Hugin `.pto`; for photogrammetry RealityCapture /
RealityScan sidecars and masks, a Metashape reference file, a COLMAP known-pose
model with a run script, and an HTML spin viewer.

## Licence

Free software, (C) 2026 Martin P. Heigan, licensed 
[CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/legalcode).
See [LICENSE.md](LICENSE.md).

edelkrone, HeadONE and SliderONE are trademarks of their owner. digiCamControl,
RealityCapture, RealityScan, Agisoft Metashape, COLMAP, PTGui, Hugin,
Papywizard, Canon, Nikon and other names are the property of their owners and
are used only to describe compatibility.

## Security

The exe is signed with a Certum code signing certificate, RFC 3161 timestamped,
and was submitted to Microsoft (WDSI) and VirusTotal before release. Each
release carries `SHA256SUMS.txt` and a signed catalogue (`release_manifest.cat`).

## Keyboard shortcuts


|Key                              |Action                                |
|---------------------------------|--------------------------------------|
|Esc                              |STOP -- halts all motion on every unit|
|Shift (while dragging a joystick)|keep to the axis you started on       |
|Ctrl+Q                           |exit                                  |

## Safety

The tool moves real equipment. Keep the motion path clear of people and
objects, and know where STOP is before you press START.

## More tools

<https://anti-matter-3d.com/tools/>
