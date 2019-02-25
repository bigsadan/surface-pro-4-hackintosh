# surface-pro-4-hackintosh-10.14.3
Perfect! 除全球无解的触摸屏，内置WIFI蓝牙摄像头外，己解决所有问题，近乎完美
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
