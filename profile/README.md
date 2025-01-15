# LiBwrt项目说明

- 本项目是基于openwrt项目针对高通深度定制的openwrt系统
- 本质上它跟官方openwrt及immortalwrt没太多区别，所以不要问哪个更好，它们都是一个东西
- 在openwrt上及immortalwrt上因为某些原因是不支持高通的NSS功能的，在此结合了qosmio库里对高通NSS的支持，合并优化成为LiBwrt以适配更多的机型和插件
- 目前LiBwrt已经对6.12内核进行了完全适配，对比6.6内核它有更低的延迟以及更好的内存优化
- 在进行了两个月的适配及优化后，目前6.12内核已经完全稳定可用了

## 其中对于高通NSS的wikiWiki
- [什么是NSS?](https://github.com/qosmio/openwrt-ipq/blob/qualcommax-6.x-nss-wifi/README.md#whats-nss)
- [OpenWrt如何“分载”流量？](https://github.com/qosmio/openwrt-ipq/blob/qualcommax-6.x-nss-wifi/README.md#how-does-openwrt-offload-traffic)
- [NSS与OpenWrt的“分载”选项有何不同？](https://github.com/qosmio/openwrt-ipq/blob/qualcommax-6.x-nss-wifi/README.md#how-is-nss-different-from-openwrts-offloading-options)
- [我需要NSS吗?](https://github.com/qosmio/openwrt-ipq/blob/qualcommax-6.x-nss-wifi/README.md#do-i-need-nss)
- [我的设备支持NSS吗？](https://github.com/qosmio/openwrt-ipq/blob/qualcommax-6.x-nss-wifi/README.md#ok-i-want-nss-does-my-device-support-it)
- [重要提示](https://github.com/qosmio/openwrt-ipq/blob/qualcommax-6.x-nss-wifi/README.md#important-note)

---

## feeds使用来源：
- packages https://github.com/immortalwrt/packages.git 
- luci https://github.com/immortalwrt/luci.git
- routing https://git.openwrt.org/feed/routing.git
- telephony https://git.openwrt.org/feed/telephony.git
- video https://github.com/openwrt/video.git
- nss_packages https://github.com/LiBwrt/nss-packages.git

## 代码来源：
- https://github.com/openwrt/openwrt
- https://github.com/qosmio/openwrt-ipq

## 更新日志

2025.1.15
 1. 修复aliyun ap8220 https://github.com/LiBwrt/openwrt-6.x/pull/76
 2. 同步主线openwrt

2025.1.14
 1. 修复基于skb的内存回收机制，减少内存占用及时回收内存
 2. 恢复IPQ settings默认设置
 3. 同步主线openwrt

