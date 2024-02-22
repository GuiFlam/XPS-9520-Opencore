# Dell XPS 9520 macOS Ventura with OpenCore

## Details

| OpenCore Version | 0.9.5 |
| --- | --- |
| macOS Version | 13.6 (Ventura) |
| SMBios | MacPro7,1 |

## Hardware Specifications

| Hardware | Specification | Status |
| --- | --- | --- |
| CPU | Intel Core i9-12900HK | ✅ Working |
| RAM | 16GB | ✅ Working |
| Audio | Realtek ALC3281 | ✅ Working |
| WiFi | Killer 1675 (AX211) | ✅ Working |
| Bluetooth | AX211 Wi-Fi 5 | ✅ Working |
| SSD | 500GB SSD | ✅ Working |
| Keyboard | - | ✅ Working |
| Trackpad | - | ✅ Working |
| Fingerprint Sensor | Shenzen Goodix | 🔶 Partially working |
| GPU | Intel Iris Xe Graphics | ❌ Not Working |
| Display | 1920 x 1200 FHD LCD | ✅ Working |

## BIOS Settings

| Setting | Option |
| --- | --- |
| SATA Operation | AHCI |
| Fast Boot | Thorough |
| Secure Boot | Disabled |
| TMP 2.0 Security | Disabled |
| Intel SGX | Disabled |
| VT for Direct I/O | Disabled |
| Fingerprint Reader | Disabled |

## UEFI IFR edits
Ahead of installing, as with other hackintoshes you will need to disable 
CFG_LOCK using modGRUBshell as follows:

```bash
setup_var_cv CpuSetup 0x43 0x00
```

## Misc
To allow the laptop to function in clamshell mode, you need to press Fn+F8 
on the clover boot menu to switch to the external display. That way the 
laptop LVDS screen is switched off and the external monitor is on. You 
need to connect a USB/Bluetooth mouse and keyboard, but the setup is much 
more practical in this way.
