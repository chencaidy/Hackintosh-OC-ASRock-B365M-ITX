# Hackintosh-OC-ASRock-B365M-ITX

## 平台配置

* 主板：ASRock B365M-ITX/ac
* CPU：Intel Core i7-8700B (Coffee Lake)
* dGPU：AMD Radeon RX580 8GB
* 网卡：Apple BCM94360CS2
* 内存：32GB DDR4 2666MHz

## 特性

* 仿冒机型：MacPro7,1（SN已去除，需自行补充）
* 系统版本：Sequoia 15.2
* 独显输出正常，最高支持4屏输出（3DP+1HDMI）
* 扬声器、麦克风输出正常，声卡ID：5
* WiFi正常，需要OCLP修补
* 蓝牙正常，支持接力，支持随航
* 睡眠正常，支持电能小憩
* USB端口正常，端口属性正确修正
* CPU电源管理正常，支持功率报告
* 支持开机音效
* 电源按钮正常，短按1S睡眠，长按>3S弹出关机对话框
* EC（SuperIO）正常，支持风扇转速报告

## 已知问题

* 需要使用OCLP进行无线网卡修补

## BIOS配置（版本：P4.30）

* 恢复出厂设置：`Exit`->`Load UEFI Defaults`
* 启用Handoff：`Advanced`->`USB Configuration`->`XHCI Hand-off`->`Enabled`
* 关闭CSM：`Boot`->`CSM (Compatibility Support Module)`->`CSM`->`Disabled`

## 更新日志

### 2024-12-30

* 更新OpenCore 1.0.3
* 更新AMFIPass 1.4.1
* 更新AppleALC 1.9.3
* 更新IntelMausi 1.0.8
* 更新IOSkywalkFamily 1.2.0
* 更新Lilu 1.7.0
* 更新NVMeFix 1.1.2
* 更新RestrictEvents 1.1.5
* 更新VirtualSMC 1.3.4
* 更新WhateverGreen 1.6.9
* 增加SMCRadeonSensors
* 开启WoL

### 2023-11-10

* 更新OpenCore 0.9.6
* 更新AppleALC 1.8.7
* 更新Lilu 1.6.7
* 更新NVMeFix 1.1.1
* 更新RestrictEvents 1.1.3
* 更新VirtualSMC 1.3.2
* 更新WhateverGreen 1.6.6
* 增加IO80211FamilyLegacy，用于支持Wi-Fi网络
* 增加IOSkywalkFamily，用于支持Wi-Fi网络
* 增加AMFIPass，绕过系统完整性检查
* 禁用SecureBootModel和SIP，用于OCLP打补丁
* 增加ResetNvramEntry选项，用于重置SMC

### 2023-02-26

* 更新OpenCore 0.8.9
* 更新AppleALC 1.7.9
* 更新Lilu 1.6.3
* 更新WhateverGreen 1.6.4

### 2022-11-23

* 更新OpenCore 0.8.6

### 2022-10-06

* 更新OpenCore 0.8.5
* 更新AppleALC 1.7.5
* 更新RestrictEvents 1.0.9

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
