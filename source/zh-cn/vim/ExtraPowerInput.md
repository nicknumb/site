title: Khadas VIM外部供电
---

**说明：**
 * 设备主要由USB-C口供电。
 * 确保适配器电压最高为5.2V，电流推荐值为2000mA。

### 概述
khadas VIM 设计了两个主要电源输入口
 * USB-C：用于供电外的同时也可以用于USB的数据传输。
 * VIN：仅用于外部供电，紧挨着USB-C口的4-Pin的电源输入口。
 * USB-C旁边还有一个USB口作为备用电源输入。

### 使用VIN作为外部供电
VIN供电口规格参数：4-Pin 1.25mm间距。
![Image of Extra_Power_VIN_Port](/images/vin_extra_power.png)
提示：我们目前还没有VIN接口的电源线售卖，需要用户自己DIY。

### 使用USB host作为外部供电
如图所示：需要准备一个公对公的USB线进行外部供电。
![Image of Male2Male_USB_Extra_Power](/images/male2male_usb_extra_power.png)

提示：
 * USB-C旁边的USB口输入电流可达900mA，可作为外部供电口，靠近网口的另外一路USB口输入电流只有500mA。具体细节请参考原理图。

### 更多资料
[VIM接口描述](/zh-cn/vim/VimInterfaces.html)

