# hackintosh-ideapad-3-14ABA7
## Intro
![About This Mac](https://media.discordapp.net/attachments/974199826063425556/1157947671689048125/vSPrkMw.png)

|          | Version                 |
|----------|-------------------------|
| OpenCore | 0.9.5                   |
| macOS    | Ventura 14.0 (23A44)  |

- Supported macOS versions: In theory this should work with any version supported by NootedRed, however only Ventura and Sonoma has been tested.
- Booting Sonoma (14) requires the 0.9.5 version.

## Info / Disclaimer
### Info
- `boot-args` used: `-v keepsyms=1 debug=0x100 swd_panic=1 npci=0x2000 revblock=media`
- `alcid`: `11`
- SMBIOS: `MacBookPro16,3`
- ~~`ShowPicker`, `ScanPolicy` and `HideAuxilary` are set up in a way that automatically boots to a APFS partition with macOS installed without user confirmation. Adjust accordingly for installation (that's why you should read the guide).~~ You should still read the guide regardless.
- NootedRed is not included, as it will be outdated anyway. Get it from its repository's [actions tab](https://github.com/ChefKissInc/NootedRed/actions)
### Usage
- You can use it however you like, except for commercial purposes (such as work environments and reselling your Hackintosh), refer to the [Psystar case](https://en.wikipedia.org/wiki/Psystar_Corporation). TLDR, you'll get your ass sued if you do so.
- Reminder that this is only a base for your OpenCore setup and should always be viewed as incomplete, and it is strongly recommended that you follow the entire OpenCore guide [here](https://dortania.github.io/OpenCore-Install-Guide/). 
- **DO NOT USE ANY INSTALLER NOT FROM APPLE**, no one knows if/how they've been tampered with, and they *always* break the APFS system volume seal, which breaks OTA updates, and are generally not trustworthy at all.
### Issues
- Stock Realtek 8822CE Wi-FI and Bluetooth DOES NOT work. Replace with an Intel or native Broadcom card if you want full functionality.
- Wake from sleep does not work.
- ~Audio over HDMI doesn't work. [#76](https://github.com/NootInc/NootedRed/issues/76)~ Works with the latest builds of NootedRed.
- General instability when using ~~GPU-intensive~~ OpenGL applications and Chromium - based browsers / Electron apps. ~~[#13](https://github.com/NootInc/NootedRed/issues/13)~~ resolved with the lastest build of NRed. Workaround for now is to use Safari.
### Notes
- Don't use case-sensitive APFS if you want to use Steam or Adobe tools.
- After installation, open System Preferences and go to Displays -> Color, uncheck `Show profiles for this display only`, then select `sRGB IEC61966-2.1`, this will make your colors look *somewhat* right (definitely not calibrated or anything but yeah, not an 
oversaturated mess)
 
![color](https://media.discordapp.net/attachments/885809091459575828/966112499487346718/unknown.png)
## Hardware

|                                           | Specifications                                                                | macOS Compatibility                                                                                                                   |
| ----------------------------------------- | ----------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| ``CPU``                                   | AMD Ryzen 5 5625U, 6 Cores / 12 Threads, 2.3GHz / 4.3GHz, 16MB L3 Cache | With native power management|
| ``Memory``                                | 16GB DDR4-3200MHz                                  |                                                                                                                                               |
| ``GPU``                                   | AMD Radeon Vega 7                                                       | With full QE/CI (Graphics accleration), VRAM (UMA Buffer Size) set to 2GB|
| ``Storage``                               | Micron MTFDKCD256TFK                                              |                                                                                                                                              |
| ``Screen``                                | 14.0" 1080p 60Hz, TN                                            |                                                                                                                                               |
| ``Webcam``                                | Integrated HD Webcam                                                          | Works!|
| ``WiFi``                                  | Intel(R) Dual Band Wireless AC 3160                                                        | Works with Airportitlwm.kext                                                                |
| ``Bluetooth``                             | Intel                                                                         | Works. |
| ``Input & Output``                        | USB 3.0 (USB-A) x1 + USB 3.1 (USB-C) x1 + USB 2.0 (USB-A) x1<br>HDMI 1.4                    | USB map provided. |
| ``Audio``                            | Realtek ALC257                                                      |                                                                                                                                               |
| ``Battery``                               | 40Wh Lithium-ion                                                                  | Battery readout works.|
| ``Keyboard``                              | -||
| ``Touchpad``                              | ELAN(?) I2C Precision Touchpad                                                                | No issues.                                                                                            |
| ``Dimensions``<br>``Weight``<br>``Power`` | 324.2 x 215.7 x 19.9<br>1.43kg<br>65W Power Adapter                        | ACPI patches won't help with these.|

Special thanks to:
- [acidanthera](https://github.com/acidanthera) - the maker of OpenCore and your favourite kexts, for making this Hackintosh possible in the first place
- [NootInc](https://github.com/NootInc) - the maker of NootedRed, bringing graphics acceleration for AMD Vega iGPUs
- [dortania people](https://github.com/orgs/dortania/people) for the OpenCore Install Guide

readme prouldly ~~stolen from~~ inspired by [beerpiss](https://github.com/beerpiss/dell-vostro-15-3568-hackintosh)'s

