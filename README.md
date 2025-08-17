# Dell Precision-5550 macOS with OpenCore

# 基本设置



| OpenCore Version | 1.0.5           |
| ---------------- | --------------- |
| macOS Version    | 26.0 (Tahoe)    |
| SMBios           | MacBook Pro16,4 |

# 硬件



| Hardware           | Specification                      | Status        |
| ------------------ | ---------------------------------- | ------------- |
| CPU                | Intel Core i9-10885H               | ✅ Working     |
| RAM                | DDR4 64GB                          | ✅ Working     |
| Audio              | Realtek ALC3281                    | ✅ Working     |
| WiFi               | AX201                              | ✅ Working     |
| Bluetooth          | AX201 Wi-Fi 5                      | ✅ Working     |
| SSD                | WD Blue SN570 2TB SSD Media 2TB    | ✅ Working     |
|                    | J.ZAO 5 SERIES 2TB SSD Media       | ✅ Working     |
| Keyboard           | -                                  | ✅ Working     |
| Trackpad           | I2C Connection                     | ✅ Working     |
| Webcam             | Microdia RGB IR HD camera          | ✅ Working     |
| MicroSD Card       | RTS5260 Card Reader                | ✅ Working     |
| Fingerprint Sensor | Shenzen Goodix                     | ❌ Not Working |
| S4 SLeep           | Hibernate/Wake                     | ✅ Working     |
| GPU                | Intel HD630 Graphics               | ✅ Working     |
| Display            | 3840 x 2400 UHD LCD(内置)          | ✅ Working     |
|                    | 3840 x 2160 (外接显示器 RV200plus) | ✅ Working     |



# BIOS 设置



| Setting            | Option   |
| ------------------ | -------- |
| SATA Operation     | AHCI     |
| Fast Boot          | Thorough |
| Secure Boot        | Disabled |
| TMP 2.0 Security   | Disabled |
| Intel SGX          | Disabled |
| VT for Direct I/O  | Disabled |
| Fingerprint Reader | Disabled |

BIOS 

```
setup_var PchSetup 0x16 0x00 # Disable RTC Memory Lock
setup_var CpuSetup 0x3E 0x00 # Disable CFG Lock
setup_var CpuSetup 0xDA 0x00 # Disable Overclocking Lock
setup_var SaSetup  0xF5 0x02 # DVMT Pre-allocated = 64MB
setup_var SaSetup  0xF6 0x03 # Total DVMT = MAX
```



# 声卡 补丁

OCLP-Mod 3.0 给声卡打上补丁即可



# 多系统启动







# 咨询







# 其他



