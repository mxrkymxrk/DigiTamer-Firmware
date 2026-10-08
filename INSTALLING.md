# Installing DigiTamer

## Public distribution model

DigiTamer is distributed to end users as prebuilt firmware. Normal users do not need the private source repository or a local build environment.

## First installation

The installation flow is:

1. Connect a supported DigiTamer device to a computer over USB.
2. Open the official DigiTamer browser installer.
3. Select the matching hardware target.
4. Select the device's ESP32-S3 serial port.
5. Start installation.
6. Allow the device to reboot.
7. Configure Wi-Fi locally from the device setup access point when prompted.

Do not disconnect power while firmware is being written.

## Important: upgrading from 0.1.x to 0.2.x

**DigiTamer 0.2.0 requires a one-time USB flash when upgrading from a 0.1.x build.**

The OTA trust bundle changed in 0.2.0. Older 0.1.x firmware does not contain the certificate trust required to securely retrieve the new update metadata, so it cannot bootstrap this upgrade over Wi-Fi.

Use the browser installer for the 0.2.0 upgrade. Once a device is running 0.2.x, compatible later releases are intended to update normally through DigiTamer's signed Wi-Fi updater.

## Updates

After Wi-Fi has been configured and the device is on the current OTA trust generation, compatible releases are intended to update directly from the device.

The updater verifies the board identifier, release metadata, authenticated HTTPS transport, cryptographic release authorization, and firmware SHA-256 integrity before the new image is accepted. DigiTamer uses separate A/B OTA application slots so the active application is not overwritten in place.

## Recovery

USB recovery remains available if an update fails or the device does not boot.

For the AIPI Lite development target, recovery generally requires entering ESP32-S3 bootloader mode and reflashing the official installation package. If normal USB flashing does not detect the device, unplug USB, hold the internal BOOT button, reconnect USB while holding it, wait about three seconds, then release BOOT and retry the installer.

## Data preservation

Routine firmware updates are designed to preserve NVS-backed pet state, DigiDex progress, settings, and local Wi-Fi configuration. A full flash erase, factory reset, or installer operation that explicitly erases the device can remove this data.

## Safety

Only use firmware explicitly marked for your hardware. Installing a binary for another board can cause boot failure or incorrect peripheral behavior.

Read [TERMS.md](TERMS.md) before installation.
