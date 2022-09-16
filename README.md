# Hackintosh-OC-ASRock-B365M-ITX

## 平台配置

* 主板：ASRock B365M-ITX/ac
* CPU：Intel Xeon E-2186M (Coffee Lake)
* iGPU：Intel UHD Graphics P630
* dGPU：AMD Radeon RX580 8GB
* 网卡：Apple BCM94360CS2
* 内存：32GB DDR4 2666MHz

## 特性

* 仿冒机型：Macmini8,1（SN已去除，需自行补充）
* 系统版本：Monterey 12.6
* 核显编解码加速正常，显卡FB：3E9B0000，VRAM：1536MB
* 独显输出正常，最高支持4屏输出（3DP+1HDMI）
* 扬声器、麦克风输出正常，声卡ID：5
* WiFi正常，免驱
* 蓝牙正常，支持接力，支持随航
* 睡眠正常，支持电能小憩
* USB端口正常，端口属性正确修正
* CPU电源管理正常，支持功率报告
* 支持开机音效
* 电源按钮正常，短按1S睡眠，长按>3S弹出关机对话框
* EC（SuperIO）正常，支持风扇转速报告

## 已知问题

* 无

## BIOS配置（版本：P4.30）

* 恢复出厂设置：`Exit`->`Load UEFI Defaults`
* 开启核显：`Advanced`->`Chipset Configuration`->`IGPU Multi-Monitor`->`Enabled`
* 启用Handoff：`Advanced`->`USB Configuration`->`XHCI Hand-off`->`Enabled`

## 更新日志

### 2022-09-17

* 更新OpenCore 0.8.3
* 更新AppleALC 1.7.4
* 更新Lilu 1.6.2
* 更新NVMeFix 1.1.0
* 更新VirtualSMC 1.3.0
* 更新WhateverGreen 1.6.1
* 设定机型Macmini8,1
