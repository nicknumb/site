title: 通过命令行方式创建系统烧录卡
---

本教程是指导linux用户一步一步地创建TF烧录卡，你也可以使用[Windows方式创建烧录卡](/zh-cn/vim/UpgradeViaTFBurningCard.html)

### 准备工作
* 编译或[下载](/zh-cn/vim/Firmware.html)最新的U-Boot文件。
* 准备好TF卡和读卡器。
* 如果TF卡上有多个分区的话，需要[通过fdisk格式化TF卡](/zh-cn/vim/CreateBurnCardViaCLI.html)。

### 开始前
如果TF卡有多个分区
```
gouwa@Wesion:~$ ls /dev/sdb*
/dev/sdb  /dev/sdb1  /dev/sdb2
gouwa@Wesion:~$ 
```
则要先删除其它分区
```
fdisk /dev/sdb
```

### 制作TF烧录卡
**把TF卡接到电脑上，并确保接上去的TF卡处于未挂载状态:**
```
$ umount /dev/sdb1
```
**把TF卡格式化为FAT32格式:**
```
$ sudo mkfs.vfat /dev/sdb1 
```
**使用"dd"工具把bootloader/u-boot写入到TF卡的第一扇区**
```
$ sudo dd if=u-boot.bin.sd.bin of=/dev/sdb conv=fsync,notrunc bs=1 count=444
$ sudo dd if=u-boot.bin.sd.bin of=/dev/sdb conv=fsync,notrunc bs=512 skip=1 seek=1
```
_说明：编译出来的U-Boot文件，其中“u-boot.bin.sd.bin”是用于制作 TF卡的，而“u-boot.bin”是用于eMMC启动的。_

**复制系统固件到TF卡上:**
重新拔插一下TF卡并运行以下命令:
```
$ cp -a aml_sdc_burn.ini Vim_Marshmallow_160928/update.img /media/gouwa/9CE9-3938/
```
 _说明:"aml_sdc_burn.ini"是u-boot烧录/下载固件到eMMC的配置文件 。_

**安全移除TF卡:**
```
$ sudo eject /dev/sdb
```
至此，TF烧录卡的制作已完成。

### 通过TF烧录卡升级固件
1. 把制作好的烧录卡插入VIM/VIM2设备中，然后上电。
2. 参考[文档](/zh-cn/vim/HowtoBootIntoUpgradeMode.html)进入升级模式。
3. 等待升级完成。

### 更多资料
* [通过命令行创建LibreELEC启动卡](/zh-cn/vim/CreateLibreELECBootCardViaCLI.html)
* [启动卡VS烧录卡](/zh-cn/vim/BootingCardVsBurningCard.html)

