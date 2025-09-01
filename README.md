# Rebirth-of-Linksys-WRT1900-AC
Linksys WRT 1900 AC installed by OpenWRT latest official build in 2025.

Linksys WRT 1900 AC重生记

第一阶段：初出茅庐（2016-2017）

时间回溯到2016年，第一次听说OpenWrt是在Koolshare论坛，获知OpenWrt系统可以部署在路由器上，并以开源闻名。经过一番了解，得知Linksys是当时原生支持部署OpenWrt系统的路由器之一，Cisco旗下品牌，参数强、名头大，最终于2016年9月购入Linksys WRT 1900 AC（v2）路由器，成功刷入NemoAlex大佬提供的OpenWrt 15.05.1 固件和相关科学上网软件包。

第二阶段：几经沉浮（2018-2024）

很快，科学上网的DNS解析出现问题，无法连接外网，需要更新插件，前提是要更新OpenWrt系统。当年的OpenWrt系统开发可谓“八仙过海各显神通”，项目分支多，有官方版本、分支（LEDE）版本和第三方版本。起步不难，很快就选取了WinSCP和Putty作为SSH登录方式（沿用至今）。因为惧怕刷机不当导致路由器变砖，在选择固件时，优先考虑维护频率和交流反馈两大要素，最终选取了由David502大佬维护的第三方版本。得益于Linksys WRT1900 AC的双系统机制，一个系统保留原厂固件，另一系统专刷OpenWrt固件，过程顺利，成功后按照飞羽大佬的教程，部署了更新的科学上网软件包（Shadowsocks + ChnRoute方案）。2019年5月，David502大佬因个人原因不再维护第三方项目，Openwrt的官方后续版本因使用反馈不佳（诸如mwlwifi无线适配和千奇百怪的bug），固件定格在David502大佬维护的一个版本，未再更换。2023年，科学上网协议特征被识别、封控，表现为访问外网时好时坏，严重影响体验。9月，家中路由器更换为华硕GT-AX6000。2024年上半年，Linksys WRT1900 AC路由器放置到办公室使用，科学上网处于完全瘫痪状态。

第三阶段：重获新生（2025-今）

时间来到2025年，闲余时间增多，同时OpenWrt系统趋于稳定，Linksys WRT 1900 AC仍在维护名单之列，于是研究重新部署。7月刷入24.10.1版本，Overlay空间23MB，装妥依赖后，能放入OpenClash的v0.46.086软件包。随着OpenClash的快速迭代，功能逐渐增多，文件逐步增大，Overlay可用空间捉襟见肘，OpenClash勉强能够运转。8月采用U盘方案尝试扩容，起初错误理解挂载和传输命令，Overlay空间被完全占满，路由器文件全部只读且无法更改。在重新梳理后，利用OpenWrt官方的在线编译固件功能，更改依赖dnsmasq为dnsmasq-full，刷入24.10.2版本，依赖安装完毕后即挂载U盘，挂载成功，Overlay空间扩容至57G，OpenClash终成完全体，科学上网跟上新时代。虽然Linksys WRT 1900 AC的WiFi传输协议已然落后时代（2.4G频道WiFi 4，5G频道WiFi 5），但实际体验和WiFi 6传输协议的差别并明显（可流畅观看YouTube 4K），至此重获新生。

特此记录，以备不虞。
