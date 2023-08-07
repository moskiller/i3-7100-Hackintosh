# i3-7100-Hackintosh
i3-7100 Gigabyte H110M-S2(ver1.0) Hackintosh


### 电脑配置

规格|详细信息
:----:|:----:
电脑型号 |	组装、台式
操作系统 |	macOS Ventura 13.5(22G74)
处理器 |	Intel(R) Core(TM) i3-7100 @3.90GHz
主板 | 技嘉 Gigabyte H110M-S2 (Ver1.0)
内存 |	8GB DDR4 2133MHz (4G*2)
硬盘 | 七彩虹 Colorful SSD 160G STATIII硬盘
集成显卡 | Intel HD Graphics 630 1536MB
集成声卡 | Realtek ALC887
显示器	| SAMSUNG LF24T35 显示器 / 1920x1080
有线网卡 | Realtek8111 100/1000M 自适应网卡，集成
引导方案 | OpenCore V0.9.3
SMBIOS | iMac19,2

### 更新日志
* 2023/08/07
  第一次上传. 


### 正常工作

1. 显卡: 集显　Intel(R) UD Graphics 630正常，注入 AAPL,ig-platform-id -> Data -> 00001259。
2. USB: 采用 Hackintool 定制，正常使用。
3. 声卡: 型号为ALC887，注入ID：1。
4. 有线网卡: 使用 Realtek8111.kext


### 安装教程 : 略，请自行上网搜索


### 注意事项
BIOS设置：  
关闭：  
1. CFG Lock（MSR 0xE2 写保护）此项必须关闭，如果你的 BIOS 里没有此项，注意设置 Kernel -> AppleXcpmCfgLock 为 Yes。
2. Intel SGX Intel Platform Trust
3. Intel Platform Trust
4. Secure Boot
5. Fast Boot
6. VT-d（可以开启，但前提是 Kernel -> DisableIoMapper 设置为 Yes）
7. CSM 
  
开启： 
1. VT-x
2. Above 4G decoding
3. Hyper-Threading
4. Execute Disable Bit
5. EHCI/XHCI Hand-off
6. OS type：Other（如果你选择 Other 会导致 CSM 联动开启，选择 Windows 8.1/10 UEFI Mode）
7. DVMT Pre-Allocated：64MB 及以上


### 下一步计划
将原来笔记本电脑上的的 BCM94360CS2 网卡拆下来，搞个转接卡怼进去...


### 鸣谢(排名不分先后)
[Apple](https://www.apple.com/)的 MacOS  

[headkaze](https://www.insanelymac.com/forum/profile/1364628-headkaze/) 提供的工具：[hackintool](https://github.com/headkaze/Hackintool) 

[Acidanthera](https://github.com/acidanthera) 提供的 OpenCore 和 相关驱动  

[github.com](https://www.github.com)  

......
