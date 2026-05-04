<div align="center">
             <h1>ROG B550-A Gaming OpenCore EFI</h1>
             <a href="README-zh_CN.md">🇨🇳中文版 Readme</a>
</div>

# Hardware Specifications
- **Motherboard**: ASUS ROG Strix B550-A Gaming (BIOS V3636)
- **CPU**: AMD Ryzen 5 3500X (6-Core)
- **RAM**: Asgard ROG Strix "Strix" Edition DDR4 3600 8GB x2 (CXMT Die)
- **GPU**: Sapphire Nitro+ AMD Radeon RX 580 8GB GDDR5 2304SP
- **Ethernet**: Intel I225-V 2.5Gbps (Onboard)
- **Wireless**: Broadcom BCM943602CS (PCI-E Adapter)
- **Audio**: Realtek ALC1220A (Onboard)

# Status
- [x] Apple Services (iCloud/iMessage/FaceTime)
- [x] GPU Hardware Acceleration (Metal 2/3)
- [x] CPU Power Management (AMDRyzenCPUPowerManagement)
- [x] USB Ports
- [x] Wi-Fi & Bluetooth
- [x] Sleep / Wake
- [x] Onboard Audio

- [ ] Onboard Intel I225-V 2.5Gbps Ethernet (Likely driver compatibility issues in macOS 14-26)

---

- **macOS Tahoe (26)**
<img width="1920" height="1080" alt="macOS_Tahoe_Screenshot" src="https://github.com/user-attachments/assets/f4a6b5f6-4dbe-4929-b093-161c51f39a74" />

# OpenCore Information
- **OpenCore Version**: V1.0.7

- **Kexts**:
<img width="1309" height="689" alt="Kexts_List" src="https://github.com/user-attachments/assets/577901a9-64ae-40f7-8983-1e1349285a45" />

- **SMBIOS**: MacPro7,1
<img width="1309" height="689" alt="SMBIOS_Info" src="https://github.com/user-attachments/assets/c6a9cdb6-e222-4ac1-a8b4-4cd574ea7934" />

# Installation Guide
### 1. BIOS Settings (Before Installation):
**Enable**
- Above 4G Decoding
- ErP Ready

**Disable**
- Fast Boot 
- CSM 
- SVM 
- TPM 
- AMD fTPM

**Adjust**
- SATA Mode -> **AHCI**
- Secure Boot -> **Other OS**

### 2. Booting
Configure your OpenCore boot entry and boot directly into the prepared macOS Recovery device.

### 3. Disk Setup
Format your target disk to **APFS** using Disk Utility, then proceed with the installation.

### 4. Post-Installation
After entering the system, use the latest version of [OCLP-Mod](https://github.com/laobamac/OCLP-Mod/releases) to download and install the **OS KDK** and apply **Root Patches**.

### 5. SMBIOS
Use proper tools to inject your own Serial, MLB, and UUID to activate Apple Services.

### 6. Enjoy!
