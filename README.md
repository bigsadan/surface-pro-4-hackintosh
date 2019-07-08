# surface-pro-4-hackintosh-10.14.x
Perfect! 除全球无解的触摸屏，内置WIFI蓝牙摄像头外，己解决所有问题，近乎完美
## Update 10.14.5
* 更新clover及kext至最新版本；
* 适配10.14.5,使用install.plist安装，安装完成后重建缓存，再切换成config.plist；
* 1600x1066 hidpi分辨率使用稳定，没有10.14.3中的花屏和睡眠缩放问题，voodooi2c使用2.1.5版本。
![mojave10.14.5](https://github.com/bigsadan/surface-pro-4-hackintosh-10.14.3/blob/master/screenshot/10.14.5.jpg)
## Update 2019.04.17
* 更新voodooi2c至最新2.1.5版本
* 增加hidpi自定义分辨率：
    * 默认的分辨率为1368 * 912 hidpi，显示效果不错但是可视面积较小，添加了几个等比缩放的HIDPI分辨率
    * 注意：调整分辨率可能导致黑屏，后果自负哦。。请三思而后行！！！如黑屏，需要外接显示器，然后装上TEAMVIEWER，断开外接显示器，重启后用手机通过teamviewer连上，改回正确分辨率即可恢复正常。
    * 具体步骤如下：
    * 1、执行以下命令确保成功。
    sudo defaults write /Library/Preferences/com.apple.windowserver DisplayResolutionEnabled -bool YES
    * 2、将DisplayVendorID-4C83.zip 解压，得到一个文件夹，文件夹里面有一个文件，获取你显示器的VendorID 和 ProductID（hackintool中可看到或获取你显示器的EDID查看），将文件夹名称后四位改成你的vendorId（后四位），文件名后四位改成你的productId（后四位)，复制到/System/Library/Displays/Contents/Resources/Overrides/
    * 3、安装RDM，选择你需要的分辨率即可（有闪电标志的为HIDPI）。
    * 分辨率添加方法说明：用PlistEdit Pro打开上述2中的文件，展开scale-resolutions，添加子键，类型为Data，值有四组8位的十六进制，每组计算的结果不足八位在前面补0，如添加1440 * 960 HIDPI分辨率，将1440 * 2十进制转换成十六进制得出 0xB40，960 * 2 由十进制转换成十六进制得出 0x780，则该分辨率对应的值为：00000B40 00000780 00000001 00200000
    * SP4的物理分辨率2736 * 1824，等比缩放的常见分辨率有：1920 * 1280    1600 * 1066    1440 * 960，我附件中的文件己添加部分hidpi，大家可以根椐需要自行换算和添加，在尝试几组后，1440 * 960比较能接受，1600 * 1066也还好，再往上太小且有卡顿不推荐。
## 配置信息
* CPU：i5-6300U
* 内存：8GB
* 硬盘：256G
* 其它：sp4 typecover
## 安装信息
* 系统：10.14.3 mojave
* clover：4871
* lilu：1.3.3
* whatevergreen：1.2.6
* voodooi2c：2.1.4
* appleALC：1.3.5
* appleBatteryManager：1.90.1
## 完成进度
* 显卡驱动正常，成功hidpi，外接屏幕输出正常
* 亮度调节正常，亮度保存正常
* 声卡工作正常，睡眠唤醒后工作正常
* SD卡槽工作正常
* 电池电量显示正常，正确识别电源适配器，正确识别电源/电池状态切换（难点1，通过DSDT修改解决）
* 自动/手动睡眠正常，合盖睡眠正常，合盖后打开唤醒正常（难点2，通过DSDT修改解决）
* 触摸板&键盘工作正常，完美支持所有系统手势（难点3，修改voodooi2c源码解决）
* 系统里所有功能均正常使用。
## 目前无解（未来估计也无解）
* 触摸屏；内置WIFI/蓝牙；摄像头
## 安装说明
安装过程全程使用config sp4-install.plist，一直到进入系统完成设置，完成安装后再使用config.plist驱动
## 截图
![mojave](https://github.com/bigsadan/surface-pro-4-hackintosh-10.14.3/blob/master/screenshot/mojave%2010143.jpg)
## 感谢
所有kext作者，还有我
