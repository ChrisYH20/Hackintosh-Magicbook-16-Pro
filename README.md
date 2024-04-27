# Hackintosh-Magicbook-16-Pro
This is a Hackintosh EFI with magicbook-16-Pro


## 支持版本

OpenCore 版本：0.9.7

目前仅在macOS13测试过，建议安装macOS12~13，mac14尚未测试~~

## 我的硬件

-CPU: AMD R7-5800H
-GPU0: NVIDIA GeForce GTX 1650
-GPU1: AMD Radeon(TM) Graphics
-主板：HONOR HYM-WXX-PCB
-固态：西数 SN730（512G）
-网卡：~~原厂（高通 WCN685x WI-FI 6E）~~ 已更换	Intel(R) Wi-Fi 6E AX210
-声卡：Conexant Synaptics Audio(具体型号：Conexant CX8070 @ AMD K19.5 - Audio Processor )

理论来说同型号电脑，换过网卡就可以直接通用，不必完全相同。

## 兼容性（半完美黑苹果）

### 目前正常运行的有
- [x] 声卡 (板载) / 网卡 (板载)
- [x] 显卡 (核显) / 硬解 4K (貌似不完全)
- [x] WiFi (PCI-E 设备) / 蓝牙 (PEI-E 载 USB 设备)
- [x] FaceTime / iMessage


### 目前异常的有

- [ ] 睡眠后无法唤醒。
- [ ] 靠近屏幕一侧的usb口和Type-c接口无法使用
- [ ] 隔空投送 / 接力无法使用（需要博通拆机网卡）

当然无法使用的那个Type-c接口可以用来日常充电使用，若有使用多个usb接口的场景，可以考虑买个HUB。
