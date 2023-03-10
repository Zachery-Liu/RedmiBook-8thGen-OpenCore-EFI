# RedmiBook-8thGen-OpenCore-EFI

## đ Language/language
[English](/) | [įŽäŊä¸­æ](/README.md) 

(Translated with DeepL)
 #### for Redmibook 8 generation i7 CPU version (8 generation i5 is theoretically universal)

 (all original without any hardware replacement)
 
 (configuration principle can run as long as the big guys do not spray)
 
 (Welcome to test and modify, welcome PR and Issue)

 ## Original EFI

 I am taking the old EFI modified from the previous version made by others, the original EFI [see here] [EFI].

 It seems that the original version is supported by gestures, maybe I messed it up, I hope some big brother can help me change it!

 
 ## Detailed configuration.

 | Hardware Name | Model |
 | :-----:| :----------------: |
 | CPU | Intel Core I7-8565U (Whiskey Lake architecture) |
 | Motherboard | TIMI-1814 |
 | Sound card | Realtek ALC256 |
 | NIC | Intel Wireless AC-9624 |
 | Display Card | Nvidia MX250 (no solution blocked)
 | Graphics | Intel Graphics UHD620 |
 | Memory | Samsung 8G 2400Mhz |
 | Hard Drive | Samsung PM871B SSD 512G (MZNLN512HAJQ-00000) |

 ## Test result

|Hardware|Status|Remarks|
|:----:|:----:|:----:|
|Wireless|â Support|Native mode driver, no Heliport|
|Bluetooth|â Support |Support Bluetooth headset, AirDrop not tested|
|Sleep with lid|â Support|Please use with caution [HiDPi][HiDPi] may cause sleep wake up shrinkage, splash screen and other issues|
|USB|â Support|Custom USB, problems may require re-customization|
|Power management|â Support|native support|
|Sound|â Support|Native test perfect, Layout ID 17|
|Touchpad|âģ Not fully supported|Touch only, gestures not working|
|HDMI output|â Supported| Test can connect to TV|
|DISCRIPTION|â Not supported|MX250 No solution, shield|
|Microphone|đ¤ˇ Not tested| Seems to be invalid|

## Version testing

OpenCore version : 0.8.8

macOS version : Ventura 13.2 (22D49)

## Other notes

USB may need to customize it yourself, as in [link][USB].

If you have headphone (sound card) problem, you can modify the alcid in boot-args, and try one by one according to the layout value in [codec table][codec], until you find the right one.

Here are the current layout values for ALC256.
5, 11, 13, 14, 16, 17, 19, 20, 21, 22, 23, 24, 28, 33, 56, 57, 66, 67, 68, 69, 70, 76, 77, 88, 97, 99

** need to replace the serial number, UUID and other data, default is empty. **

The functions and enablement of each component are roughly shown in the figure (there may be inaccurate and modified parts, subject to the actual)

ACPI

! [ACPI][ACPI]

Kext

! [Kext][Kext]

[USB]: https://macx.top/26316.html
[ACPI]: /Readme_img/SCR-20230207-fg2.png
[Kext]: /Readme_img/SCR-20230207-fhg.png
[HiDPi]: https://github.com/xzhih/one-key-hidpi
[EFI]: https://macx.top/16960.html
[codec]: https://github.com/acidanthera/AppleALC/wiki/Supported-codecs
[english]: /README.EN.md


