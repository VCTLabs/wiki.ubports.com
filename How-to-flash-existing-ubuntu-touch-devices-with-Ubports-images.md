-----------------

## You probably want a different page than this

This page has been rolled into our newer, better page, [[How to install UBports on Your Device|How-to-install-UBports-on-your-device]]

-----------------


**NOTE: THIS METHOD WILL WIPE YOUR DATA! PLEASE BACKUP BEFORE TRYING, We are working on a method that will not wipe your data, if you want to keep your data please wait until that's done or you use this backup method:**
1. Ensure ssh-server is installed on backup destination
```
sudo apt install openssh-server
```
2. Create the destination folder on your backup destination
3. Ensure your phone can connect to your backup destination (e.g. both in same LAN)
4. Backup your phone
```
rsync -avz --delete /home/phablet/ <user>@<server>:<dirname>/phablet/
```
**to send all Apps data to your server of choice, and later reverse the process to restore the data. Then follow these steps (this will not work in a virtual machine):** 

1. Reboot to bootloader (try holding volume (down, up or both) + power button)
2. Download the unlocked adb recovery for your device
3. Install (if it isn't installed) and run ubuntu-device-flash:

```
sudo apt install ubuntu-device-flash
sudo ubuntu-device-flash --server=https://system-image.ubports.com/ touch \
--channel=15.04/stable --bootstrap \
--recovery-image=[Downloaded adb recovery image]
```

Please [[file a bug report|UBports Bug Trackers]] if you have any problem.

**NOTE: UNTESTED DEVICES MIGHT RUN INTO UNEXPECTED ISSUES, PLEASE BE PREPARED TO FIX YOUR DEVICE**

### Unlocked adb recovery:

BQ Aquaris E4.5
Codename: krillin
Status: <span style="color:green">Works, tested</span>
Adb recovery: http://cdimage.ubports.com/devices/recovery-krillin.img

BQ Aquaris E5
Codename: vegetahd
Status: <span style="color:green">Works, tested</span>
Adb recovery: http://cdimage.ubports.com/devices/recovery-vegetahd.img

BQ Aquaris M10 HD
Codename: cooler
Status: <span style="color:green">Works, tested</span>
Adb recovery: http://cdimage.ubports.com/devices/recovery-cooler.img

BQ Aquaris M10 FHD
Codename: frieza
Status: <span style="color:green">Works, tested</span>
Adb recovery: http://cdimage.ubports.com/devices/recovery-frieza.img
*If flashing fails, try [this](https://forums.ubports.com/topic/263/can-t-get-the-m10-fhd-to-take-the-flash/3).*
*NOTE: this device seem to use little over 3 minutes to boot, [we are looking into this issue](https://github.com/ubports/ubports-touch/issues/53)*

Meizu MX4
Codename: m75/arale
Status: <span style="color:green">Works, tested</span>
Adb recovery: http://cdimage.ubports.com/devices/recovery-arale.img

Meizu PRO 5
Codename: turbo
Status: <span style="color:green">Works, tested</span>
Adb recovery: http://cdimage.ubports.com/devices/recovery-turbo.img