<div align="center">
             <h1>ROG B550-A Gaming OpenCore EFI</h1>
             <img src="https://img.shields.io/github/release/VisualTechStudio/ROG-B550-A-Gaming-OpenCore-EFI" />
             <img src="https://img.shields.io/github/downloads/VisualTechStudio/ROG-B550-A-Gaming-OpenCore-EFI/total?color=white&style=plastic" />
             <img src="https://img.shields.io/github/stars/VisualTechStudio/ROG-B550-A-Gaming-OpenCore-EFI" />
             <br>
             <br>
             <a href="README_en_US.md">🇬🇧English Readme</a>
</div>

# 硬件详情
- 主板:ASUS ROG Strix B550-A Gaming (BIOS V3636)
- CPU:AMD Ryzen 5 3500X (6核心)
- 内存:阿斯加特 ROG Strix 吹雪 DDR4 3600 8x2 长鑫存储
- 显卡:蓝宝石超白金 AMD Radeon RX 580 8GB GDDR5 2304SP
- 有线板载网卡:Intel I225-V 2.5Gbps
- 无线PCIE网卡:博通 BCM943602CS
- 板载声卡:Realtek ALC1220A

# 工作情况
- [x] Apple服务(iCloud/iMessage/FaceTime)
- [x] GPU硬件加速(Metal 2)
- [x] CPU电源管理(AMDRyzenCPUPowerManagement)
- [x] USB端口
- [x] Wifi和蓝牙
- [x] 睡眠/关闭显示器
- [x] 板载声卡

- [ ] 板载Intel I225-V 2.5Gbps有线网卡(似乎是OS14-26的驱动兼容性问题)

---

- MacOS Tahoe(26)
<img width="1920" height="1080" alt="微信图片_20260504223506_33_1" src="https://github.com/user-attachments/assets/f4a6b5f6-4dbe-4929-b093-161c51f39a74" />

# OpenCore信息
- OpenCore:V1.0.7

- Kexts:
<img width="1309" height="689" alt="微信图片_20260504223656_42_1" src="https://github.com/user-attachments/assets/577901a9-64ae-40f7-8983-1e1349285a45" />

- SMBios:MacPro7,1
<img width="1309" height="689" alt="微信图片_20260504223855_51_1" src="https://github.com/user-attachments/assets/c6a9cdb6-e222-4ac1-a8b4-4cd574ea7934" />

# 使用教程
1.在安装系统前设置BIOS:
开启
- Above 4G Decoding
- ErP Ready

关闭
- Fast Boot 
- CSM 
- SVM 
- TPM 
- AMDFTPM

调整
- SATA Mode - AHCI
- Secure Boot - Other OS

2.设置 OC 启动项后直接启动烧录好的MacOS Recovery设备

3.格式化磁盘至APFS后开始安装

4.进入系统后使用 https://github.com/laobamac/OCLP-Mod/releases 的最新版本下载并安装 OS KDK 和 Root Patch

5.使用工具注入三码激活Apple服务

6.开始体验
