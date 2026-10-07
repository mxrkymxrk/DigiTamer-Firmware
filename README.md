<div align="center">

# DigiTamer

### Prebuilt color virtual-pet firmware for supported ESP32 hardware

**Raise · Train · Battle · Evolve · Discover**

[![Status](https://img.shields.io/badge/status-alpha-yellow)](#release-status)
[![Distribution](https://img.shields.io/badge/distribution-prebuilt%20firmware-blue)](#installation)
[![Hardware](https://img.shields.io/badge/target-AIPI%20Lite%20%2F%20ESP32--S3-2ea44f)](#supported-hardware)
[![Installer](https://img.shields.io/badge/browser-installer-available-2ea44f)](https://mxrkymxrk.github.io/DigiTamer-Firmware/)

## [☕ Buy me a coffee](https://buymeacoffee.com/mxrkymxrk)

### [Install DigiTamer](https://mxrkymxrk.github.io/DigiTamer-Firmware/)

[Installation guide](INSTALLING.md) · [Safety & Terms](TERMS.md) · [Third-party notices](THIRD_PARTY_NOTICES.md)

</div>

---

DigiTamer is an independent, unofficial, non-commercial virtual-pet firmware project. This public repository is for **prebuilt firmware distribution and installation only**. DigiTamer implementation source is maintained privately and is not distributed here.

> **Alpha software:** features, gameplay balance, save structures, networking, and installation tooling may change before a stable release. The installer is present, but no public firmware should be treated as production-ready until a hardware-validated release is published.

## Release status

Development includes a persistent virtual-pet lifecycle, branching evolution, care mechanics, CPU battles, sound, battery monitoring, persistent DigiDex progress, Wi-Fi provisioning, A/B OTA partitions, HTTPS transport verification, SHA-256 firmware integrity checks, and signed OTA release metadata.

The target user experience is one USB installation followed by compatible Wi-Fi firmware updates.

## Installation

```text
Connect supported device by USB
        ↓
Open DigiTamer browser installer
        ↓
Flash official prebuilt firmware
        ↓
Configure Wi-Fi locally
        ↓
Raise your DigiTamer
        ↓
Future signed updates over Wi-Fi
```

No compiler, PlatformIO installation, or source checkout is required for normal users.

**Browser installer:** https://mxrkymxrk.github.io/DigiTamer-Firmware/

See [INSTALLING.md](INSTALLING.md) before flashing.

## Supported hardware

The initial reference target is the **AIPI Lite / ESP32-S3** with a 128×128 color display, ES8311 audio, battery monitoring, and Wi-Fi.

Only install firmware explicitly marked for your hardware revision. An incompatible image can prevent normal boot until recovery flashing is performed.

## Firmware authenticity and update security

Official DigiTamer builds are designed around multiple checks rather than trusting a download URL alone:

- authenticated HTTPS transport
- DigiTamer P-256 release-signing key verification
- board compatibility validation
- version metadata validation
- SHA-256 firmware verification before activation
- separate A/B OTA application slots
- post-update boot validation and rollback support
- USB recovery path

The private signing key is not stored in this public repository or embedded in firmware. The device contains only the public verification key.

Do not install firmware presented as DigiTamer from an untrusted third-party source.

## Source code

This distribution repository does **not** grant access to DigiTamer's private implementation source code.

A downloadable firmware binary is permission to use that distributed build subject to the accompanying terms. It is not a grant of ownership in DigiTamer, Digimon intellectual property, trademarks, artwork, source code, or other third-party material.

## Unofficial fan-project notice

DigiTamer is an independent fan project and is not affiliated with, sponsored by, approved by, or endorsed by Bandai, Toei Animation, Akiyoshi Hongo, or other Digimon rights holders.

Digimon, Digital Monster, Vital Bracelet, related names, characters, artwork, sprites, trademarks, and associated media are owned by their respective rights holders.

See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

## Warranty and risk

DigiTamer is experimental software provided without warranty. Installing firmware modifies embedded hardware and can result in data loss, failed boot, or the need for recovery flashing.

See [TERMS.md](TERMS.md) before installing.

---

<div align="center">

## Support independent development

If you enjoy DigiTamer or other projects I build, you can support my independent development work:

### [☕ Buy me a coffee](https://buymeacoffee.com/mxrkymxrk)

Support is voluntary. It does not purchase Digimon content, intellectual-property rights, firmware ownership, warranties, priority support, or restricted features.

[Install DigiTamer](https://mxrkymxrk.github.io/DigiTamer-Firmware/) · [Installation guide](INSTALLING.md) · [Terms](TERMS.md)

</div>
