title: Upgrade Via a USB-C Cable
---
## Upgrade On Windows
### Preparations
* Download the [USB Upgrade Tool](http://www.mediafire.com/file/mvf43ds0iacs8i7/USB_Burning_Tool_v2.0.8_x86.rar) and extract it.
* Run 'setup_v2.0.8.exe' to install the tool for VIM upgrading:
	![Image of USB_Upgrade_Tool_Setup_V208](/images/vim/usb_upgrade_tool_setup_v208.png)

### Upgrading Steps
Make sure that you have right installed the USB Upgrade Tool, then follow the below steps to upgrade:

1. Open ‘USB_Burning_Tool_v2.0.8.exe’, click ‘File-->Import image’ to chose an image for VIM.
2. Connect VIM and PC with an USB-C cable(VIM will power on automately).
3. Let VIM enter into upgrade mode to complete the upgrading:
	* Long press `Power` key without release
	* Short press `Reset` key and release
	* Count 2-3 seconds and release the `Power` key to enter into upgrade mode
4. Your PC should have found VIM device as upgrade mode if you correctly follow the above operations.

	Now all you need to do is to click `Start` button of the tool and wait the upgrading to complete:
	![Image of USB_Upgrade_Tool_Setup_V208](/images/vim/usb_upgrade_tool_interface_v208.png)

*Tips:*

* Click `Stop` button first, then close the tool to quit current upgrading operation.
* [Extra power supply](/basics/ExtraPowerInput.md) is required in some case your PC cannot provide enough current for the upgrading.

## Upgrade On Ubuntn
### Preperations
```
$ sudo apt-get install libusb-dev git parted
```
### Get burning tool
Image burning tool on Ubuntu is in repository [utils](https://github.com/khadas/utils).
```
$ git clone https://github.com/khadas/utils
```
Or just pull it if you have cloned this repository.
```
$ cd /path/to/utils
$ git pull
```
### Install burning tool
You need to install USB rules and create some links.
```
$ cd /path/to/utils
$ ./INSTALL
```
You will see this if successed.
```
Installing Amlogic flash-tool...

===============================================

Host PC: Ubuntu 16.04

===============================================

Installing USB rules...
[sudo] password for nick: 
Installing flash-tool...
Done!

Installing Rockchip flash-tool...

===============================================

Host PC: Ubuntu 16.04

===============================================

Installing USB rules...
Installing flash-tool...
Done!
Installing Khadas burn-tool...
Done!
```
**NOTE:** Root privilege required.

### Check the USB driver
You should bring your VIM board [enter upgrade mode](/vim/HowtoBootIntoUpgradeMode.html).
Check the USB driver.
```
$ lsusb | grep Amlogic
Bus 002 Device 036: ID 1b8e:c003 Amlogic, Inc.
```
The message means that your board is recognized.

### How to burn image on Ubuntu
```
$ burn-tool -i /path/to/image
```
You will see the logs if successed.
```
Rebooting the board ........[OK]
Unpacking image [OK]
Initializing ddr ........[OK]
Running u-boot ........[OK]
Create partitions [OK]
Writing device tree [OK]
Writing bootloader [OK]
Wiping  data partition [OK]
Wiping  cache partition [OK]
Writing boot partition [OK]
Writing data partition [OK]
Writing logo partition [OK]
Writing system partition [OK]
Do you want to reset the board? y/n [n]? y
Resetting board [OK]

```
And you can add parameter `--debug` to print debug infomation.For more usage please refer to [docs](https://github.com/khadas/utils/tree/master/aml-flash-tool/docs).

### Uninstall burning tool
```
$ cd /path/to/utils
$ ./UNINSTALL
```

**NOTE:**This burning tool has only been verified on **Ubuntu 16.04**.

### See also
* [Upgrade Via a TF Burning Card](/vim/UpgradeViaTFBurningCard.html)
* [Howto Boot Into Upgrade Mode](/vim/HowtoBootIntoUpgradeMode.html)

