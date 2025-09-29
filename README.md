Here's your corrected `README.md` file with the code block removed from the top and all assistant-specific language removed:

---

# 📱 Moto G10 / G10 Power / Lenovo K13 Note Custom ROM

## 🔐 Features

* ✅ **SELinux**: Enforcing
* ✅ **Play Store Certified**
* ✅ **GApps**: Pre-included
* ✅ **Moto Apps**: Pre-installed:

  * Moto Audio Recorder
  * Moto Camera 3
  * Moto Clock
  * Moto Gallery
  * Moto Interactive Wallpapers
  * Moto Widget

---

## ⚙️ Installation Guide

### 📦 Prerequisites

1. **Unlock your bootloader**
   Visit the official Motorola page and follow the instructions:
   [Unlock Bootloader](https://en-us.support.motorola.com/app/standalone/bootloader/unlock-your-device-a)

2. **Download Required Files**
   Go to the [Releases Page](https://github.com/Deivid21/RELEASES/blob/main/README.md#moto-g10--g10-power--lenovo-k13-note-capri) and download:

   * `boot.img`
   * `dtbo.img`
   * `vendor_boot.img`
   * `vbmeta.img`
   * `vbmeta_system.img`
   * ROM `.zip` file

---

### 🛠️ Flashing Boot Images

1. Reboot into bootloader:

   ```bash
   adb reboot bootloader
   ```

2. Flash the images:

   ```bash
   fastboot flash boot boot.img
   fastboot flash dtbo dtbo.img
   fastboot flash vendor_boot vendor_boot.img
   fastboot flash vbmeta vbmeta.img
   fastboot flash vbmeta_system vbmeta_system.img
   fastboot reboot recovery
   ```

---

### 📁 Ensuring Firmware Partition Consistency

1. Download **copy-partitions-20220613-signed.zip**:
   [LineageOS Tools](https://mirrorbits.lineageos.org/tools/copy-partitions-20220613-signed.zip)

2. In recovery, navigate to:

   ```
   Apply update -> Apply from ADB
   ```

3. Flash the partition tool:

   ```bash
   adb -d sideload copy-partitions-20220613-signed.zip
   ```

---

### 🧹 Factory Reset & ROM Flash

1. Reboot into recovery.

2. Navigate to:

   ```
   Factory reset -> Format data/factory reset
   ```

   Confirm the format.

3. Return to the main menu, then go to:

   ```
   Apply update -> Apply from ADB
   ```

4. Flash the ROM:

   ```bash
   adb -d sideload rom.zip  # Replace "rom" with actual filename
   ```

---

## 🔄 Updating the ROM

1. Reboot into recovery.

2. Navigate to:

   ```
   Apply update -> Apply from ADB
   ```

3. Flash the updated ROM:

   ```bash
   adb -d sideload rom.zip  # Replace "rom" with actual filename
   ```

---

## 📲 OTA Updates

1. Check for updates via system settings.

2. If an update is available:

   * Select **Download and install**
   * Wait approximately 10–15 minutes

3. Reboot when the installation completes.

---

## 💬 Credits

Maintained by [@Deivid21](https://github.com/Deivid21)

---
