# Installing DigiTamer

## Public distribution model

DigiTamer is distributed to end users as prebuilt firmware. Normal users do not need the private source repository or a local build environment.

## First installation

The target installation flow is:

1. Connect a supported DigiTamer device to a computer over USB.
2. Open the official DigiTamer browser installer.
3. Select the matching hardware target.
4. Select the device's ESP32-S3 serial port.
5. Start installation.
6. Allow the device to reboot.
7. Configure Wi-Fi locally from the device setup access point when prompted.

Do not disconnect power while firmware is being written.

## Updates

After Wi-Fi has been configured, compatible releases are intended to update directly from the device.

The updater verifies the board identifier, release metadata, transport security, cryptographic release authorization, and firmware integrity before the new image is accepted.

DigiTamer uses separate OTA application slots so the active application is not overwritten in place.

## Recovery

USB recovery remains available if an update fails or the device does not boot.

For the AIPI Lite development target, recovery generally requires entering ESP32-S3 bootloader mode and reflashing the official installation package.

## Data preservation

Routine firmware updates are designed to preserve NVS-backed pet state, DigiDex progress, settings, and local Wi-Fi configuration. A full flash erase or factory-reset procedure can remove this data.

## Safety

Only use firmware explicitly marked for your hardware. Installing a binary for another board can cause boot failure or incorrect peripheral behavior.

Read [TERMS.md](TERMS.md) before installation.
