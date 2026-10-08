<div align="center">

# DigiTamer

### Prebuilt color virtual-pet firmware for supported ESP32 hardware

**Raise · Train · Battle · Evolve · Discover**

[![Status](https://img.shields.io/badge/status-alpha-yellow)](#release-status)
[![Version](https://img.shields.io/badge/version-0.2.0--alpha-b9ff39)](#release-status)
[![Distribution](https://img.shields.io/badge/distribution-prebuilt%20firmware-blue)](#installation)
[![Hardware](https://img.shields.io/badge/target-AIPI%20Lite%20%2F%20ESP32--S3-2ea44f)](#supported-hardware)
[![Installer](https://img.shields.io/badge/installer-online-brightgreen)](https://mxrkymxrk.github.io/DigiTamer-Firmware/)

## [☕ Buy me a coffee](https://buymeacoffee.com/mxrkymxrk)

### [Install DigiTamer](https://mxrkymxrk.github.io/DigiTamer-Firmware/)

[Installation guide](INSTALLING.md) · [Safety & Terms](TERMS.md) · [Third-party notices](THIRD_PARTY_NOTICES.md)

</div>

---

DigiTamer is an independent, unofficial, non-commercial virtual-pet firmware project. This public repository is for **prebuilt firmware distribution and installation only**. DigiTamer implementation source is maintained privately and is not distributed here.

> **Alpha software:** features, gameplay balance, save structures, networking, and installation tooling may change before a stable release. Hardware behavior should be considered experimental until validated on the target device.

## Release status

**0.2.0-alpha is a major firmware update.** It expands DigiTamer from the initial VPet prototype into a substantially broader digital-pet system with a redesigned interface and content pipeline.

Highlights include:

- persistent virtual-pet lifecycle with care, training, health and battle state
- branching evolution content across **53 trees**, **930 species records**, and **624 DigiDex entries**
- redesigned Home, Status, System, Settings, Network and Firmware screens
- stage-based pixel-art environments and framebuffer-based rendering
- DigiDex grid, filtering and evolution-tree selection
- animated CPU battles
- expanded button navigation including previous/fast-scroll and sleep shortcut
- redesigned Wi-Fi setup portal with scanning and captive-portal behavior
- background audio task, volume preview and additional UI/game sound events
- A/B OTA partitions, HTTPS verification, signed update metadata and SHA-256 firmware integrity checks
- expanded OTA certificate trust bundle and time synchronization before secure update requests

### One-time USB upgrade from 0.1.x

**Devices running DigiTamer 0.1.x must install 0.2.0 over USB once.** The OTA trust bundle changed in 0.2.0, and older firmware cannot securely bootstrap the new certificate chain. After moving to 0.2.x, compatible later releases are intended to use the normal signed Wi-Fi updater.

See [INSTALLING.md](INSTALLING.md) for the migration and recovery procedure.

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
Future compatible signed updates over Wi-Fi
```

No compiler, PlatformIO installation, or source checkout is required for normal users.

**Browser installer:** https://mxrkymxrk.github.io/DigiTamer-Firmware/

## Supported hardware

The initial reference target is the **AIPI Lite / ESP32-S3** with a 128×128 color display, ES8311 audio, battery monitoring, buttons, and Wi-Fi.

Only install firmware explicitly marked for your hardware revision. An incompatible image can prevent normal boot until recovery flashing is performed.

## Firmware authenticity and update security

Official DigiTamer builds are designed around multiple checks rather than trusting a download URL alone:

- authenticated HTTPS transport with an embedded CA trust bundle
- DigiTamer P-256 release-signing key verification
- board compatibility and version metadata validation
- SHA-256 firmware verification before activation
- separate A/B OTA application slots
- post-update boot validation / recovery path
- USB recovery installation

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
