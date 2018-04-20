title: 通过Windows电脑安装LibreELEC
---

### 准备工作
* [x] 下载 [Win32DiskImager](https://sourceforge.net/projects/win32diskimager/)。
* [x] 解压并安装到Windows电脑上
* [x] 一张TF卡和一个TF卡读卡器。

注意：若是TF卡里面有数据要提前备份出来，制作过程会格式化整个TF卡。

### 下载固件
1. 运行Win32DiskImager
2. 插入TF到电脑上，电脑有识别到TF卡的盘符
3. 选择固件，并确认已经选择正确的TF卡盘符，然后点击"write":
![Image of Win32DiskImagerLibreELEC.jpg](/images/Win32DiskImagerLibreELEC.jpg)
4. 操作完成后，安全移除TF卡。

### 从TF启动
由于 Khadas VIM/VIM2支持多种启动方式（TF卡，U盘，板载eMMC），所以当两种以上启动方式同时在用时，要知道手动设置启动项的方法。启动刚才所制作的TF启动卡可选择发下方式：
1. 长按“Function”键，从TF卡启动（需要更新到最新固件）
2. [清空eMMC](/zh-cn/vim/HowtoEraseEMMC.html)，VIM/VIM2会自动从TF卡启动。
3. 强制进入 [MaskRom模式](/zh-cn/vim/develop/HowtoBootIntoUpgradeMode.html)，Khadas VIM/VIM2会尝试从TF卡启动。

提示：
* 确保TF卡可制作成引导卡，并写入正确的固件
* Khadas VIM/VIM2的第一引导介质是eMMC，所以有引导的固件在eMMC上面的话，会优先从eMMC启动。
* “Function”键模式：硬件会先从eMMC启动，然后再通过软件方式加载TF卡上的固件进行切换。

### 更多资料
* [通过命令行方式创建LibreELEC的TF引导卡](/zh-cn/vim/CreateLibreELECBootCardViaCLI.html)

