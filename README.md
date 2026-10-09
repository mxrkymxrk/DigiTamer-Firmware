<div align="center">

# DigiTamer

### Prebuilt color virtual-pet firmware for AIPI Lite / ESP32-S3

**Raise · Train · Battle · Evolve · Play · Connect**

[![Status](https://img.shields.io/badge/status-alpha-yellow)](#release-status)
[![Version](https://img.shields.io/badge/version-0.2.7--alpha-b9ff39)](#release-status)
[![Distribution](https://img.shields.io/badge/distribution-prebuilt%20firmware-blue)](#installation)
[![Hardware](https://img.shields.io/badge/target-AIPI%20Lite%20%2F%20ESP32--S3-2ea44f)](#supported-hardware)
[![Installer](https://img.shields.io/badge/installer-online-brightgreen)](https://mxrkymxrk.github.io/DigiTamer-Firmware/)

## [Install DigiTamer](https://mxrkymxrk.github.io/DigiTamer-Firmware/)

[☕ Buy me a coffee](https://buymeacoffee.com/mxrkymxrk) · [Installation guide](INSTALLING.md) · [Safety & Terms](TERMS.md) · [Third-party notices](THIRD_PARTY_NOTICES.md)

</div>

---

DigiTamer is an independent, unofficial, non-commercial virtual-pet firmware project. This public repository contains **prebuilt firmware, installer files, signed update metadata, and public documentation only**. DigiTamer implementation source is maintained separately.

> **Alpha software:** gameplay balance, save structures, networking, battery behavior, and installation tooling may still change before a stable release.

## Release status

The current public build is **0.2.7-alpha**.

DigiTamer has grown well beyond the initial VPet prototype. The current firmware combines persistent care and evolution with RPG-style progression, multiple pets, mini-games, local multiplayer systems, a bilingual UI, secure OTA updates, and more aggressive battery-saving behavior.

### Current highlights

- persistent virtual-pet lifecycle with hunger, happiness, strength, effort, health, sickness, waste, weight, care mistakes, and sleep-aware care
- **53 evolution trees**, **930 species records**, and **624 DigiDex entries**
- deterministic evolution driven by species, care, health, effort, mistakes, battles, and win rate
- Levels **1-99**, XP, trainer rating, and trainable **ATK / DEF / SPD**
- animated CPU battles from Baby II upward with Easy / Even / Hard challenges
- signature battle moves and a persistent named Rival
- up to **3 pet slots**, with one active pet and inactive pets safely frozen
- **Hall of Fame** records for retired/deceased partners and **Daycare** support
- training mini-games: **Punch**, **Lift**, and **Run**
- Arcade games: **Digi-Catch**, **Memory Match**, and **Pattern**, with high scores and capped daily rewards
- English and Spanish UI, including first-boot language selection
- new food presentation and animations for **Fish, Berry, and Shake**
- DigiDex grid, filters, detail views, and evolution-tree browsing
- multiple saved Wi-Fi networks and on-demand connectivity
- Wi-Fi **off by default** when not needed, with opportunistic activation for network features to reduce battery drain
- LAN PvP, LAN trading, co-op training, opponent history, and challenge-card systems implemented for same-network devices
- protocol trust hardening including pet IDs, duplicate reconciliation, verified co-op input logs, and descriptor plausibility checks
- signed OTA updates with P-256 signature verification, SHA-256 integrity checks, HTTPS trust validation, and A/B firmware slots

### 0.2.7 changes

0.2.7 focuses on polish and battery-aware interaction:

- added Fish, Berry, and Shake food icons and feed animations
- moved **Arcade** into the Home action flow
- moved Wi-Fi setup into **Settings**
- Wi-Fi now stays off by default and activates only when a network feature needs it
- documentation and diagnostics were aligned with the current build

### Recent 0.2.x additions

The releases leading into 0.2.7 also added:

- multiple saved Wi-Fi networks and Evo Boost
- LAN PvP battles and battle-health tuning
- 3-pet slot management and additional battery-saving behavior
- English/Spanish localization
- daily care streaks and item-management/trainer mechanics
- Hall of Fame and Daycare
- deterministic training mini-games
- LAN trading and opponent records
- LAN co-op training
- signature moves and a persistent Rival
- multiplayer trust hardening
- the three-game Arcade and reward system

> **Multiplayer note:** local-network systems are implemented, but some two-device behavior may still require field verification on physical hardware.

## One-time USB upgrade from 0.1.x

**Devices running DigiTamer 0.1.x must install 0.2.0 or later over USB once.** The OTA trust bundle changed in 0.2.0, and older firmware cannot securely bootstrap the new certificate chain.

After that migration, compatible 0.2.x releases can use DigiTamer's signed Wi-Fi updater.

See [INSTALLING.md](INSTALLING.md) for migration and recovery.

## Installation

```text
Connect supported device by USB
        ↓
Open DigiTamer browser installer
        ↓
Flash official prebuilt firmware
        ↓
Choose language / configure settings
        ↓
Raise your DigiTamer
        ↓
Use Wi-Fi only when network features are needed
        ↓
Future compatible signed updates over Wi-Fi
```

No compiler, PlatformIO installation, or source checkout is required for normal users.

**Browser installer:** https://mxrkymxrk.github.io/DigiTamer-Firmware/

## Supported hardware

The current reference target is the **AIPI Lite / ESP32-S3** with:

- 16 MB flash
- 8 MB PSRAM
- 128×128 color LCD
- ES8311 audio
- two physical buttons
- battery monitoring
- Wi-Fi
- A/B OTA application slots

Only install firmware explicitly marked for your hardware revision. An incompatible image can prevent normal boot until recovery flashing is performed.

## Firmware authenticity and update security

Official DigiTamer builds use multiple checks instead of trusting a download URL alone:

- authenticated HTTPS transport with an embedded CA trust bundle
- DigiTamer P-256 release-signing verification
- board compatibility and version metadata validation
- SHA-256 firmware verification before activation
- separate A/B OTA application slots
- post-update boot validation / recovery path
- USB recovery installation

The private signing key is not stored in this public repository or embedded in firmware. Devices contain only the public verification key.

Do not install firmware presented as DigiTamer from an untrusted third-party source.

## Distribution model

This repository is intentionally limited to the public distribution surface:

```text
DigiTamer-Firmware
├── browser installer
├── prebuilt firmware
├── signed update manifest
├── checksums
├── installation documentation
├── terms / notices
└── public project information
```

The implementation source is not distributed from this repository.

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
