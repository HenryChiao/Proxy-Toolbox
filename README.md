# 代理工具箱 (Proxy Toolbox)

> **2025 年最新版跨平台代理工具与生态清单**
> 拒绝过时信息，梳理一份涵盖移动端、桌面端、软硬路由及周边生态的“与时俱进”指南。

[![Last Updated](https://img.shields.io/badge/Last%20Update-2025--12--06-green)](https://github.com/henrychiao/proxy-toolbox)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

---

## 📖 关于本项目 (About)

市井流传的 App 清单大多停留在 Clash 删库前 (2023.10) 的旧时代。本仓库由**海豚测速**维护，旨在建立一份 2025 年标准的代理工具选型指南。

**核心覆盖：**
* **内核 (Cores):** Mihomo (Clash.Meta), Sing-box, Xray, V2ray
* **平台 (Platforms):** Android, iOS, Windows, macOS, Linux, Routers
* **生态 (Ecosystem):** 规则集, 订阅转换, 小工具



---

## 🧭 导航目录 (Navigation)

### 1. 核心与客户端 (Cores & Clients)
本仓库主要内容按**代理内核**分类。如果您不确定选择哪个内核，请先阅读 [选型建议 (Roadmap)](roadmap/README.md)。

| 核心分类 | 特点简述 | 包含平台文档 |
| :--- | :--- | :--- |
| [**📂 Sing-box**](cores/sing-box/README.md) | ⚡ **极致性能**，全协议支持，DNS处理最强。配置门槛稍高。 | Android, iOS, Win, Mac, Linux, Router |
| [**📂 Mihomo**](cores/mihomo/README.md) | 🛡️ **生态丰富**，原 Clash.Meta。分流规则易用，兼容性最好。 | Android, iOS, Win, Mac, Linux, Router |
| [**📂 Xray / V2ray**](cores/xray/README.md) | 🧪 **自建首选**，协议更新快 (Reality/HY2)，稳守底层。 | Android, iOS, Win, Router |
| [**📂 Hybrid / 框架**](cores/hybrid/README.md) | 📦 **多核集合**，如 Nekobox 等同时支持多种核心的工具。 | Android, Win, Linux |

### 2. 路由与进阶 (Routers & Advanced)
| 模块 | 说明 |
| :--- | :--- |
| [**📂 路由器方案**](cores/sing-box/routers.md) | 包含华硕梅林、小米官方固件、OpenWrt 软路由插件推荐。 |
| [**📂 规则集**](rulesets/README.md) | GeoIP, GeoSite, 广告拦截规则, 分流规则 (适用于各内核)。 |
| [**📂 辅助工具**](tools/README.md) | Sub-Store (订阅管理), Script Hub, SubCase 等小工具。 |
| [**📂 订阅转换**](converters/README.md) | 推荐的在线/本地订阅转换服务列表。 |

---

## 🏆 快速推荐 (Quick Picks)

如果您不想深入研究，请直接参考以下“闭眼入”的 2025 年度推荐：

### 📱 移动端 (Mobile)
* **Android:**
    * 👑 首选：**FlClash** (Mihomo系，美观) 或 **Sing-box** (官方版，极致)
    * 🛠 自建：**Nekobox**
* **iOS:**
    * 👑 首选：**Shadowrocket** ($2.99 全能王)
    * 💎 专业：**Surge** ($49.99/年 体验天花板)

### 🖥 电脑端 (Desktop)
* **Windows:** **Clash Verge Rev** (易用) 或 **v2rayN** (老牌全能)
* **macOS:** **Surge Mac** (软路由平替) 或 **FlClash** (轻量化)

### 🛜 路由器 (Router)
* **华硕:** MerlinClash2 (需刷梅林)
* **小米:** ShellCrash (需解锁 SSH)
* **OpenWrt:** OpenClash (功能全) 或 Nikki (轻量)

---

## 🗺️ 选型路线图 (Roadmap)

> 详见 [roadmap/README.md](roadmap/README.md)

* **基础需求** (流动场所 + 单设备) ➡️ **手机 App**
* **甜点需求** (固定场所 + 多设备 + 易用性) ➡️ **华硕/小米硬路由 + 插件**
* **进阶需求** (极致分流 + 双重极致体感) ➡️ **OpenWrt + Sing-box/TCP调优**

---

## 📝 附录 (Appendix)

* [📊 App ⇆ 协议速查表](appendix/protocol-matrix.md)
* [🌐 DNS / Fake-IP / Real-IP 说明](appendix/dns.md)
* [🚀 TCP 调优 / 单线程瓶颈说明](appendix/performance.md)

---

## 🤝 反馈与更新 (Feedback)
