title: Upgrade Via a USB-C Cable
---

### Preparations
* Download the [USB Upgrade Tool](http://www.mediafire.com/file/mvf43ds0iacs8i7/USB_Burning_Tool_v2.0.8_x86.rar) and extract it.
* Run 'setup_v2.0.8.exe' to install the tool for VIM upgrading:
	![Image of USB_Upgrade_Tool_Setup_V208](/images/usb_upgrade_tool_setup_v208.png)

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
	![Image of USB_Upgrade_Tool_Setup_V208](/images/usb_upgrade_tool_interface_v208.png)

*Tips:*

* Click `Stop` button first, then close the tool to quit current upgrading operation.
* [Extra power supply](/basics/ExtraPowerInput.md) is required in some case your PC cannot provide enough current for the upgrading.


Have Fun!

### See also
* [Upgrade Via a TF Burning Card](/vim/UpgradeViaTFBurningCard.html)
* [Howto Boot Into Upgrade Mode](/vim/HowtoBootIntoUpgradeMode.html)
