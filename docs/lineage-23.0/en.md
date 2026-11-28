# Installation guide

> [!WARNING]
> You will lose all your data. **Back up your data before flashing.**

## Requirements
* Unlocked bootloader
* PC

## Flashing

1. Flash [this](https://github.com/NightlyLI6/releases/releases/tag/fox_r12.0_1_knukima) OrangeFox:

   ```sh
   fastboot flash vendor_boot --slot=all recovery.img
   fastboot reboot recovery
   ```

2. Select **Menu → ADB & Sideload**. 

    **You MUST check the "Reflash OrangeFox after flashing a ROM" option. Otherwise, you will not be able to boot into the system. If you forgot to select this option, reflash the recovery to both slots, then switch to the slot where the ROM was installed.**


3. Sideload the ZIP:

   ```sh
   adb sideload <filename.zip>
   ```

4. Format data via Yes

5. If you want to install additional packages (GApps, kernel), reboot into recovery first to change boot slot!

6. Done.