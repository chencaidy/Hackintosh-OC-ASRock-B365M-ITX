# Hackintosh-OC-ASRock-B365M-ITX

## 平台配置

* 主板：ASRock B365M-ITX/ac
* CPU：Intel Core i7-8700B (Coffee Lake)
* iGPU：Intel UHD Graphics 630
* dGPU：AMD Radeon RX580 8GB
* 网卡：Apple BCM94360CS2
* 内存：32GB DDR4 2666MHz

## 特性

* 仿冒机型：MacPro7,1（SN已去除，需自行补充）
* 系统版本：Monterey 12.6
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

## 初次安装注意

第一次安装macOS或者硬盘抹掉后，会在苹果LOGO后无限重启（Verbose模式下第一屏代码跑完后立即重启）,因为此OC默认启用SecureBoot机制

解决方法如下：

1. 编辑config.plist，将`SecureBootModel`修改为`Disabled`
2. 正常安装macOS
3. 安装完成后，将`SecureBootModel`改回`j160`

## BIOS配置（版本：P4.30）

* 恢复出厂设置：`Exit`->`Load UEFI Defaults`
* 启用Handoff：`Advanced`->`USB Configuration`->`XHCI Hand-off`->`Enabled`
* 关闭CSM：`Boot`->`CSM (Compatibility Support Module)`->`CSM`->`Disabled`

## 更新日志

### 2022-09-22

* 更新OpenCore 0.8.4
* 更新AppleALC 1.7.5
* 更换机型为MacPro7,1
* 更新BIOS配置，默认禁用iGPU
* 修复MacPro内存映射

### 2022-09-17

* 更新OpenCore 0.8.3
* 更新AppleALC 1.7.4
* 更新Lilu 1.6.2
* 更新NVMeFix 1.1.0
* 更新VirtualSMC 1.3.0
* 更新WhateverGreen 1.6.1
* 设定机型Macmini8,1
