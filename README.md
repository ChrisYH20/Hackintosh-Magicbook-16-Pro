# Hackintosh-Magicbook-16-Pro
This is a Hackintosh EFI with magicbook-16-Pro
![GitHub stars](https://img.shields.io/github/stars/ChrisYH20/Hackintosh-Magicbook-16-Pro?style=flat-square)
![GitHub download total](https://img.shields.io/github/downloads/ChrisYH20/Hackintosh-Magicbook-16-Pro/total?style=flat-square)
![GitHub forks](https://img.shields.io/github/forks/ChrisYH20/Hackintosh-Magicbook-16-Pro?style=flat-square)
## 支持版本

OpenCore 版本：0.9.8

目前仅在macOS13.5.2测试过，建议安装macOS12~13，mac14尚未测试~~

## 我的硬件

- CPU: AMD R7-5800H
- GPU0: NVIDIA GeForce GTX 1650
- GPU1: AMD Radeon(TM) Graphics
- 主板：HONOR HYM-WXX-PCB
- 固态：西数 SN730（512G）
- 网卡：~~原厂（高通 WCN685x WI-FI 6E）~~ 已更换 Intel(R) Wi-Fi 6E AX210
- 声卡：Conexant Synaptics Audio(具体型号：Conexant CX8070 @ AMD K19.5 - Audio Processor )

理论来说同型号电脑，换过网卡就可以直接通用，不必完全相同。

## 兼容性（半完美黑苹果）

### 目前正常运行的有
- [x] 声卡 (板载) / 网卡 
- [x] 显卡 (核显) / 硬解 4K (貌似不完全)
- [x] WiFi / 蓝牙 
- [x] FaceTime / iMessage

这里声卡id为15，亲测AMD的声卡id 15和21 均可驱动

NootedRed新版版核显驱动默认无硬解，此处使用的核显驱动来自 [果农](https://github.com/htmambo/NootedRed/releases/tag/1.0.1712425054)

![sleep_fix](/readme_src/VDA.png)

### 目前异常的有

- [ ] 睡眠后无法唤醒
- [ ] 靠近屏幕一侧的usb口和Type-c接口无法使用
- [ ] 隔空投送 / 接力无法使用（需要博通拆机网卡）
- [ ] 独显

当然无法使用的那个Type-c接口可以用来日常充电使用，若有使用多个USB接口的场景，可以考虑买个HUB。

### 更改 EFI
- 建议使用 OCAT 重新生成Pi中的序列号、UUID、ROM 等信息，避免三码冲突导致 iService 无法使用。
- 将 [EFI](/EFI/OC) 放进你的 ESP 引导分区即可。

### 注意

- 安装黑苹果前请在BIOS中关闭安全启动。

- 该款机型出厂核显默认只有512M显存，原版BIOS阉割了修改显存的功能，建议使用[UniversalAMDFormBrowser](https://github.com/DavidS95/Smokeless_UMAF)修改显存为2G及以上，否则使用过程中可能会感觉到卡顿。

## 感谢
感谢[国光](https://github.com/sqlsec)提供的教程，以及AMD核显黑苹果交流群内相关大佬的的指导（群就不放出来了）。也感谢为Hackintosh无私贡献的各位开源作者，感谢他们写的驱动。
