# GecEdu RK3568 #
## 2026.3.15 ##
**粤嵌开发板** 由底板和核心板组成，还有7寸屏幕。自带系统位Bulidroot

经拆解与底层验证，硬件实际配置如下：Machine model: Rockchip RK3568 EVB1 DDR4 V10 Board  

| 组件          | 规格                            | 状态     | 备注                                    |
| :------------ | :------------------------------ | :------- | :-------------------------------------- |
| **SoC**       | Rockchip RK3568b2               | ✅ 已验证 | 四核 Cortex-A55                         |
| **RAM**       | 2GB DDR4                        | ✅ 已验证 |                                         |
| **存储**      | 16GB eMMC                       | ✅ 已验证 | 设备节点 `/dev/block/mmcblk2`           |
| **网络**      | 1x 千兆以太网口                 | ✅ 已验证 |                                         |
| **USB**       | 3x usb2.0，1xusb3.0, 1x OTG     | ✅ 已验证 | **OTG 可用于刷机**                      |
| **无线**      | Wi-Fi 5                         | ✅ 已验证 | 可搜索网络                              |
| **视频**      | HDMI/**LVDS**                   | ✅ 可用   | LDVS连接7寸触摸屏幕                     |
| **其他**      | 1x MSATA, SIM 卡槽，SD卡槽，    | 🔍 待验证 | 功能待驱动验证                          |
| **USART/CAN** | 4xUART,1x Debug UART，1xCAN接口 |          | Debug用于查看串口日志,串口波特率1500000 |

  ![IMG_2742](E:\20250526HYL\RK3568b2\pig\IMG_2742.JPG)



出厂开发板系统包含常规的rk356x_demo软件，**`rk356x-demo` 是一个基于 LVGL 的、直接操作帧缓冲 (`/dev/fb0`) 并控制 GPIO 和背光的嵌入式图形程序。**

板子还没sdk资料。
这有我上传的dtb，不知道还需要什么资料。这个板子和正点原子的RK3568有点像。
刷入过RK3568-EVB1-V10-BUILDROOT_V1.3.0_20251220的uboot是没问题的。 目前机器的镜像是内核为4.19.232的bulidroot
CPU：RK3568
内存：2G
EMMC硬盘：16G
网口：千兆
USB2.0：3个


<img width="790" height="1054" alt="Image" src="https://github.com/user-attachments/assets/9295b2e8-55ee-44d7-90a4-553d75318a8a" />

![Image](https://github.com/user-attachments/assets/6646622e-3809-4881-91ae-f4b7b89a9f93)

<img width="790" height="592" alt="Image" src="https://github.com/user-attachments/assets/b8c26d7a-f5f8-4424-ad00-77feb4081ed1" />
