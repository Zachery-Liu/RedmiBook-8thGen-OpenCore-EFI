# RedmiBook-8thGen-OpenCore-EFI
 #### 适用于Redmibook 8代i7CPU的版本（8代i5理论上通用）

 （全原装 没有替换任何硬件）
 
 （配置原则能跑就行 大佬勿喷）
 
 （欢迎各位测试修改，欢迎 PR 和 Issue）
 
 ## 详细配置：

 | 硬件名称 | 型号 |
 | :-----:| :----------------: |
 | CPU | 英特尔 酷睿 I7-8565U （Whiskey Lake架构） |
 | 主板 | TIMI-1814 |
 | 声卡 | 瑞昱 ALC256 |
 | 网卡 | 英特尔 Wireless  AC-9624 |
 | 独显 | 英伟达 MX250（无解已屏蔽） |
 | 集显 | 英特尔 Graphics UHD620 |
 | 内存 | 三星 8G 2400Mhz |
 | 硬盘 | 三星固态 512G 具体型号忘记了 影响不大） |

 ## 使用情况

* [x] 无线网卡 （原生模式驱动，无需 Heliport ）
* [x] 蓝牙 （能驱动，未测试其他功能）
* [x] 触摸板 （仅触摸，手势无效）
* [x] 合盖睡眠 （需配合 [HiDPi][HiDPi] 修复花屏等）
* [x] 电源管理
* [x] 声音（外放完美，貌似插耳机对于网易云等音乐软件有点问题）
* [ ] 独显 （MX250 无解，屏蔽）
* [ ] 麦克风 （未测试，主要是我用不上）

## 版本及测试情况

OpenCore版本 : 0.8.8

macOS版本 : Ventura 13.2 (22D49)

## 其他说明

USB记得自己定制，方法如[链接][USB]。

需替换序列号，默认为空。

各组件功能及启用情况大致如图（可能有不准确及修改部分，以实际为准）

ACPI

![ACPI][ACPI]

Kext

![Kext][Kext]

[USB]: https://macx.top/26316.html
[ACPI]: /Readme_img/SCR-20230207-fgr.png
[Kext]: /Readme_img/SCR-20230207-fhg.png
[HiDPi]: https://github.com/xzhih/one-key-hidpi
