# 腾达 BE12 Pro · ImmortalWrt + OpenClash

本 fork 以 Sun-flower1 的 2026-10-26 Release 为基线。定制配置选择 OpenClash 0.48.002 和 ARM64 Meta 核心，移除 PassWall2、Xray 及其专用依赖。设备目标为 MT7987A + MT7992 的腾达 BE12 Pro，保留原版 LuCI、简体中文、Argon、Wi-Fi 7、WARP 和 HNAT 支持。

- [查看云编译运行与产物](https://github.com/hongzhangbqb/immortalwrt-tenda-be12-pro/actions/workflows/openwrt-builder.yml)。通过成品检查后，运行页的 Artifacts 会提供两种镜像、SHA256SUMS 和包差异。
- [查看增量配置](.config) · [查看锁定的软件源](feeds.conf.default) · [下载完整构建包和刷前说明](BE12-Pro-OpenClash-build.zip)。
- 当前工作流会解开本目录中通过 SHA-256 验证的构建包，用其中的配置、脚本和原版清单编译并核验产物。根目录的配置文件供阅读，与该包一致。修改构建参数时也要同步归档和工作流中的校验值。
- 构建包 SHA-256 为 `9a917ed9492dcab218908fbbeda74ee2ec3f7104546f254f6b7d81ce9e7513e2`。定制固件的校验值见成功运行随附的 SHA256SUMS。

原版只提供 sysupgrade 和 RAM 启动用的 initramfs。刷前核对板号、分区、容量及镜像哈希，执行只读平台测试。原厂系统或分区不符时请勿强刷。
