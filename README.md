# RedmiBook-8thGen-OpenCore-EFI

## 🌍 Language/语言
[English][english] | [简体中文](/) 

 #### 适用于Redmibook 8代i7CPU的版本（8代i5理论上通用）

 （全原装 没有替换任何硬件）
 
 （配置原则能跑就行 大佬勿喷）
 
 （欢迎各位测试修改，欢迎 PR 和 Issue）

 ## 原EFI

 我是拿以前别人做的旧版EFI修改而成，原EFI[见这里][EFI]。

 貌似原版是支持手势的，可能是被我搞没了吧，希望有大佬能帮我改下！

 
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
 | 硬盘 | 三星 PM871B 固态 512G （MZNLN512HAJQ-00000） |

 ## 使用情况

|硬件|状态|备注|
|:----:|:----:|:----:|
|无线网卡|✅ 支持|原生模式驱动，无需 Heliport|
|蓝牙|✅ 支持 |支持蓝牙耳机，AirDrop未测试|
|合盖睡眠|✅ 支持|请谨慎使用 [HiDPi][HiDPi] 可能导致睡眠唤醒缩小、花屏等问题|
|USB|✅ 支持|定制 USB，有问题可能需要重新定制|
|电源管理|✅ 支持|原生支持|
|声音|✅ 支持|本机测试完美，Layout ID 17|
|HDMI输出|✅ 支持|电视输出已测试|
|触摸板|⍻ 不完全支持|仅触摸，手势无效|
|独显|❌ 不支持|MX250 无解，屏蔽|
|麦克风|🤷 未测试|貌似无效|

## 版本及测试情况

OpenCore版本 : 0.8.8

macOS版本 : Ventura 13.2 (22D49)

## 其他说明

USB可能需要自己定制，方法如[链接][USB]。

如果有耳机（声卡）问题可以修改 `boot-args` 里的 `alcid` ，按照 [codec表][codec] 里的 `layout` 值一个一个试，直到找到合适的。

这里是目前 ALC256 的 `layout` 值：  

`5, 11, 13, 14, 16, 17, 19, 20, 21, 22, 23, 24, 28, 33, 56, 57, 66, 67, 68, 69, 70, 76, 77, 88, 97, 99`

**需替换序列号、UUID等数据，默认为空。**

各组件功能及启用情况大致如图（可能有不准确及修改部分，以实际为准）

ACPI

![ACPI][ACPI]

Kext

![Kext][Kext]

[USB]: https://macx.top/26316.html
[ACPI]: /Readme_img/SCR-20230207-fg2.png
[Kext]: /Readme_img/SCR-20230207-fhg.png
[HiDPi]: https://github.com/xzhih/one-key-hidpi
[EFI]: https://macx.top/16960.html
[codec]: https://github.com/acidanthera/AppleALC/wiki/Supported-codecs
[english]: /README.EN.md
