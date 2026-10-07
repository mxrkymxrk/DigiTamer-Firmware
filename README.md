<div align="center">

# DigiTamer

### Prebuilt color virtual-pet firmware for supported ESP32 hardware

**Raise · Train · Battle · Evolve · Discover**

[![Status](https://img.shields.io/badge/status-alpha-yellow)](#release-status)
[![Distribution](https://img.shields.io/badge/distribution-prebuilt%20firmware-blue)](#installation)
[![Hardware](https://img.shields.io/badge/target-AIPI%20Lite%20%2F%20ESP32--S3-2ea44f)](#supported-hardware)

## [☕ Buy me a coffee](https://buymeacoffee.com/mxrkymxrk)

[Installation](INSTALLING.md) · [Safety & Terms](TERMS.md) · [Third-party notices](THIRD_PARTY_NOTICES.md)

</div>

---

DigiTamer is an independent, unofficial, non-commercial virtual-pet firmware project. This public repository is intended for **prebuilt firmware distribution and installation only**. The DigiTamer source code is maintained privately and is not distributed through this repository.

> **Alpha software:** features, gameplay balance, save structures, networking, and installation tooling may change before a stable release.

## Release status

Current development includes a persistent virtual-pet lifecycle, branching evolution, care mechanics, CPU battles, sound, battery monitoring, persistent DigiDex progress, Wi-Fi provisioning work, and A/B OTA update support.

Normal users are intended to install DigiTamer once over USB and then receive future compatible firmware updates over Wi-Fi.

## Installation

The intended user flow is:

```text
Connect supported device by USB
        ↓
Open DigiTamer browser installer
        ↓
Flash prebuilt DigiTamer firmware
        ↓
Configure Wi-Fi locally
        ↓
Use DigiTamer
        ↓
Future signed updates over Wi-Fi
```

No compiler, PlatformIO installation, or source checkout is required for normal users.

See [INSTALLING.md](INSTALLING.md).

## Supported hardware

The initial reference target is the **AIPI Lite / ESP32-S3** with a 128×128 color display, ES8311 audio, battery monitoring, and Wi-Fi.

Only install firmware specifically marked for your hardware revision. Flashing incompatible firmware can make the device temporarily unusable until recovery flashing is performed.

## Firmware authenticity

Official DigiTamer releases are intended to use:

- HTTPS transport validation
- board compatibility checks
- version metadata
- SHA-256 firmware integrity verification
- cryptographically signed release metadata
- dual A/B OTA application slots
- recovery flashing over USB

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

</div>
