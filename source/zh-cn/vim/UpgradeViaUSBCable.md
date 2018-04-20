title: 通过USB-C数据线升级固件
---

### 准备工作
* 下载升级工具[USB Upgrade Tool](http://www.mediafire.com/file/mvf43ds0iacs8i7/USB_Burning_Tool_v2.0.8_x86.rar)并解压。
* 运行Run 'setup_v2.x.x.exe'程序进行安装。
![image|453x181](/images/usb_upgrade_tool_setup_v208.png) 

### 固件升级操作步骤
确保已经正确安装好升级工具，按照下面步骤进行升级：

1. 打开升级工具‘USB_Burning_Tool_v2.x.x.exe’，点击"File-->Import image"选择要升级的固件。
2. 用USB-C线连接VIM/VIM2和PC电脑（默认VIM/VIM2上电会自动开机）。
3. 进入固件更新模式
   * 长按Power键不要松开
   * 短按Rest键并松开
   * 大概3秒后松开Power键进入固件升级模式
4.  如果上面操作已正确执行，电脑端会发现VIM/VIM2升级设备，点击升级工具上的start按钮开始固件升级，升级进度条100%时完成升级。
![image|690x456](/images/usb_upgrade_tool_interface_v208.png)

提示：
* 先点击"stop"按钮再关闭升级工具。
* [外部供电要求](http://docs.khadas.com/basics/ExtraPowerInput/)，部分电脑供电比较弱会导致升级失败。

### 更多资料
 * [通过TF卡升级固件](/zh-cn/vim/UpgradeViaTFBurningCard.html)
 * [怎样进入升级模式](/zh-cn/vim/HowtoBootIntoUpgradeMode.html)

