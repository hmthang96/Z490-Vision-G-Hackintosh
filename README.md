# Z490-Vision-G-Hackintosh

My PC:
- CPU: I7- 10700
- RAM: 48Gb 3200
- Wifi - PCIE x2: BCM94360
- Audio optical - PCIE x2
- Main: Z490 Vision G
- VGA1 - PCIE x16: RX570 Shapphie Nitro 4Gb
- VGA2 - PCIE x8 GTX1660s Asus Dual 6Gb
- SSD1: WDS 1Tb
- SSD2: Intel HBR Optane 512Gb

____________________
 
My EFI work only on Z490 Vision G (not D) on Catalina, Bigsur, Monterey abd Ventura . Currently, Working on macOS Ventura 13.1


- Before using my EFI, you must use OCAuxiliaryTools to create MLB, UUID, Serial Number and ROM.
- I use iGPU for compute only!
- I disable GTX1660s on PCIE x8 (slot 2) - SSDT-GPU-Disabled.aml ( If you use this file, the slot 2 PCIE x8 will not recogize on Hackintosh)
- I disable SSD Optane 512Gb by aml file - SSDT-NVMe-Pcc.aml  (like above, the m2 slot near slot 2 PCIE will be disabled)

To make Intel 255 Lan work on Bigsur and monterey, you will flash the custom fw to this card.
From Ventura, Intel 255-V will work natively, no need to patch.

BCM94360 Wifi is temporary not working, I will fix late.

IF you use AMD card, you can play DRM on Apple TV and play lossless audio on Apple Music by below pasting code to terminal:
defaults write com.apple.AppleGVA gvaForceAMDKE -boolean yes