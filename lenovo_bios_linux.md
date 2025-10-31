# Update Lenovo BIOS from Linux

1. Visit https://support.lenovo.com and select the desired device.
2. Go to *Drivers & Software* -> *Select Drivers* -> *BIOS/UEFI* and download __BIOS Update (Bootable CD)__.
3. Download [geteltorito](https://github.com/rainer042/geteltorito) from GitHub or using your preferred package manager.
4. Run geteltorito to extract the image contents:
   ```
   geteltorito.pl -o <image>.img <image>.iso
   ```
5. Write the extracted image to USB drive:
   ```
   dd if=<image>.img of=<destination> bs=512K
   ```
6. Reboot choosing the USB drive as a temporary boot device.
7. Proceed with the on screen instructions.

##### further read
- [Flashing BIOS from Linux - ArchWiki](https://wiki.archlinux.org/title/Flashing_BIOS_from_Linux#Bootable_optical_disk_emulation)
- [How to update Lenovo BIOS from Linux without using Windows - nixCraft](https://www.cyberciti.biz/faq/update-lenovo-bios-from-linux-usb-stick-pen/)
