# Hackintosh-EFI-Dell-Latitude_7280
EFI files for Hackintosh on a Dell Latitude 7280 (2017 version)
- macOS Catalina 10.15.3
- Clover version: r5104

# Updates on 24 February 2020

- Clover updated to r5104
- macOS updated to 10.15.3
- Updated various kexts
- HDMI output fixed in config.plist, and it is now working well (audio not tested)
 
  First issue: reboots when HDMI cable is plugged in.
  
  Fix: 
  
  1) Insert fake id in Devices>Fake ID>IntelGFX: 0x591B0000
  2) Tick Graphics>Inject Intel;
  3) Select from dropdown menu: Graphics>ig-platform-id>Kabby Lake 620 0x59160000
  
  Second issue: reboot stops from above fix, but external screen is all purple.
  
  Fix:
  
  follow this: https://www.mathewinkson.com/2013/03/force-rgb-mode-in-mac-os-x-to-fix-the-picture-quality-of-an-external-monitor
  
  (Note: the reboot-into-recovery-then-disable-SIP method did not work for me, the directory S/L/D/C/R/O still not accessible even SIP is disabled. I use the reboot-into-recovery-then-copy-and-replace-via-terminal method mentioned in the first update in the post (https://www.mathewinkson.com/2013/03/force-rgb-mode-in-mac-os-x-to-fix-the-picture-quality-of-an-external-monitor/comment-page-13#comment-15886).)
  
- Camera tested working well

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
- WiFi
- Bluetooth (with BrcmBluetoothInjector.kext)
- Keyboard (supports shortcut for volume adjustment (fn+f1/f2/f3), and brightness adjustment (f2/f3) configured in settings)
- Touchpad (one-finger and two-finger gestures, do copy the "CopyToLE" files into Library/Extensions and rebuild cache)
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
