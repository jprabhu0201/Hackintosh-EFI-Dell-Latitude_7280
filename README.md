# Hackintosh-EFI-Dell-Latitude_7280 (on macOS Catalina 10.15.3)
EFI files for Hackintosh on a Dell Latitude 7280 (2017 version), updated to macOS Catalina 10.15.3

# Clover version: r5104

# Hardware

- CPU: Core i7 7600U
- GPU: Intel HD 620
- WiFi: DW1560/BCM94352Z (separately purchased to replace the original Intel hardware)
- Screen resolution: 1920X1080
- RAM: 8G
- SSD: Intel NVME 256G

# Working:

- Sidecar
- Sleep (wake by power button)
- Sound/Mic (speaker, earphone)
- Network (only wireless tested)
- Bluetooth (with BrcmBluetoothInjector.kext)
- Keyboard (supports shortcut for volume adjustment (fn+f1/f2/f3), and brightness adjustment (f2/f3) configured in settings)
- Touchpad (one finger and two finger gestures, ensure to copy the "CopyToLE" files into Library/Extensions and rebuild cache)
- HDMI output
- Camera
- Battery
- USB
- Thunderbolt (USB-C supported when plugged-in before boot, charging works)

# Not tested

- SD card reader
- Ethernet

# Credit
https://osxlatitude.com/forums/topic/12379-dell-lattitude-7480-catalina/
