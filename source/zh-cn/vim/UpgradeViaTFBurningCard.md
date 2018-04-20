title: 通过TF卡升级固件
---

### 准备工作
 * 下载[Burn Card Maker Tool](http://www.mediafire.com/file/u349mo760o1dt6i/Burn_card_maker_V2.0.2_20150617_en.7z) 并解压。
* 准备好TF卡的读卡器。
* 一台高清显示器（带HDMI接口）。

注意：若是TF卡里面有数据要提前备份出来，制作过程会格式化整个TF卡。

### 固件升级操作步骤
1. 运行工具“Burn_Card_Maker.exe”
![Image of BurnCardMaker_Tool](/images/BurnCardMaker_Tool.png)

2. 插入TF到电脑上，识别到TF的盘后：
   * 在工具的下拉框“Choose the disk”里选择TF卡设备。
   * 选择"To Partition and Format"(第一次制作TF升级卡时要选上此项)
   * 点击"Open"按钮选择要升级的固件
   * 点击"Make"按钮制作TF升级卡
![Image of BurnCardMaker_Tool_Interface](/images/BurnCardMaker_Tool_Interface.png)
3. 当所有都完成了之后，点击"Success"按钮完成当前操作。
4. 从电脑上安全移除TF卡，然后插入到VIM/VIM2的TF卡槽里面。
5. 连接好HDMI和USB-C线，然后给VIM/VIM2上电。
6. 让VIM/VIM2进入升级模式
   * 长按Power键不要松开
   * 短按Rest键并松开
   * 大概3秒后松开Power键进入固件升级模式

正常操作后，显示器上会显示以下内容：
![Image of Upgrading_Interface](/images/Upgrading_interface.png)

### 更多资料
 * [通过USB-C数据线](/zh-cn/vim/UpgradeViaUSBCable.html)
 * [怎样进入升级模式](/zh-cn/vim/HowtoBootIntoUpgradeMode.html)


