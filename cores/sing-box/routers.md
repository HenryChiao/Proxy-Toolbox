# 🛗 Routers (OpenWrt/硬路由) - Sing-box

## 🛜 硬路由 (小米 - 需解锁 SSH)

### ShellCrash
* **核心**: 可选 `Singbox` 或 `Singbox-P` (PuerNya 版) 核心。
* **缺点**: sing-box 核心使用步骤繁琐，须分成两个子配置文件。

## 🗄 OpenWrt 软路由

### PassWall / PassWall2
* **核心**: 核心任选 Xray/Singbox 等。
* **优势**: 配置弹性大、支持负载均衡。
* **缺点**: 分流实现繁琐。

### Momo Nikki (Nikki 的 singbox 版)
* **核心**: 核心可替换为支持机场订阅 provider 的 reF1nd 分支。
* **注意**: 新项目，对 TCP/UDP 模式暂不支持覆写，对 tag 命名有约束。

### HomeProxy (🟢 推荐)
* **核心**: 调用 **Singbox 核心**，由 immortalWrt 官方维护。
* **依赖**: `Firewall4/nftables`。
* **评价**: 纯粹的 Sing-box 插件。

### Neko / NekoBox
* **核心**: 可调用 Mihomo/Singbox 核心。
* **依赖**: `Firewall4/nftables`, `PHP-CGI`。

### Sing-box [裸核]
* **说明**: 若在 `Firewall4/nftables` 环境下开 `auto_redirect` 也不麻烦，性能最强。
