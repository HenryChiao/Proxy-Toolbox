# ☢️ 核心 (Kernels)

> **简介**: 所有的代理客户端（GUI）都只是外壳，真正决定性能、协议支持和分流策略的是其背后的**内核（Core）**。
>
> 不同的内核分支（如 P版、Alpha版）通常是为了解决特定环境下的痛点（如 OpenWrt 兼容性、规则集格式差异）而存在的。

---

## 1. Clash 家族 (Clashverse)

Clash 是过去五年最流行的代理架构，但目前已发生重大更替。

### 🔴 Clash Premium (原版/闭源)
* **状态**: 💀 **已死 (2023.11 删库)**
* **标识**: 通常指 Fndroid / Dreamacro 维护的原始版本。
* **特点**: 闭源，不支持 VLESS-Reality, Hysteria2, TUIC 等新协议。
* **现状**: 现存的任何“原版 Clash”内核都已过时，强烈建议替换。

### 🟢 Mihomo (原 Clash.Meta)
* **状态**: 🔥 **当前标准 (主流)**
* **维护者**: MetaCubeX
* **特点**:
    * 目前生态中兼容性最好、协议支持最全的 Clash 系内核。
    * **Mihomo Alpha/Dev**: 开发版，更新极其频繁（有时一天数更），第一时间支持新特性，但偶有 Bug。
    * **Mihomo Stable**: 稳定版，适合追求安稳的用户。
* **适用**: 几乎所有现代 Clash 客户端（Clash Verge Rev, FlClash, ShellCrash 等）。

---

## 2. Sing-box 家族

由于 Sing-box 迭代激进（尤其是 1.8 → 1.9 → 1.11 的规则集格式变更），社区出现了多个分支以适配不同的使用场景。

### 🟢 Sing-box (Official)
* **状态**: **官方正统**
* **维护者**: SagerNet / Nekohasekai
* **标识**: 官方 Release 版本。
* **特点**:
    * **纯粹**: 严格遵循官方文档，支持最新的 `srs` (v3) 规则集格式。
    * **激进**: 经常重构配置格式，导致旧配置报错。
* **适用**: 官方客户端（Android/iOS/Mac），以及追求最新特性的极客。

### 🟡 Sing-box P (PuerNya 版)
* **状态**: **兼容性改良 (OpenWrt 首选)**
* **维护者**: PuerNya
* **标识**: `Sing-box-P` / `PUER`
* **特点**:
    * **优化**: 针对 OpenWrt 软路由进行了内存和性能优化。
    * **兼容**: 修复了部分官方版在特定 ISP 环境下的连接问题。
    * **功能**: 有时会提前合并一些官方尚未发布的 PR（Pull Requests），或者保留一些被官方移除的特性。
* **适用**: **ShellCrash**, **HomeProxy** 等路由器插件环境。

### 🟠 Sing-box R / Community Builds
* **状态**: **社区编译/特定适配**
* **标识**: `Sing-box-R`, `Hiroki` 等非官方编译版。
* **特点**:
    * 这类通常是社区开发者为了适配特定 CPU 架构（如极老的 MIPS 路由器）或为了集成特定功能（如某些去广告补丁）而自行编译的版本。
* **注意**: 使用此类内核需自行承担稳定性风险。

---

## 3. 核心导航目录 (Index)

根据您的设备和需求，请进入相应目录查看详细的**客户端清单**：

| 目录 | 核心/分类 | 关键词 |
| :--- | :--- | :--- |
| **[📦 Sing-box](./sing-box/)** | **Sing-box** | 协议最全、DNS 最强、120Hz 体感、配置难 |
| **[📦 Mihomo](./mihomo/)** | **Mihomo (Meta)** | 生态最富、客户端最多、兼容性好 |
| **[📦 Xray](./xray/)** | **Xray / V2ray** | 老牌稳健、VLESS 制定者、V2rayN 标配 |
| **[📦 Hybrid](./hybrid/)** | **混合/eBPF** | Linux 软路由高性能、Android Root 框架 |
| **[📦 Proprietary](./proprietary/)** | **闭源商业** | iOS 三巨头 (Surge/Loon/QX)、极致 UI |
| **[🔁 V2ray](./v2ray/)** | *Legacy* | (指向 Xray，旧时代兼容) |

---

## ℹ️ 选型简表

* **我是 iOS 用户**: 选 **[Proprietary](./proprietary/)** (Surge/QX) 或 **[Sing-box](./sing-box/)** (官方免费)。
* **我是 Windows/Mac 用户**: 选 **[Mihomo](./mihomo/)** (Verge/FlClash) 最省心。
* **我是 软路由 (OpenWrt) 用户**:
    * 追求稳定: **[Mihomo](./mihomo/)** (OpenClash)。
    * 追求性能/新协议: **[Sing-box P](./sing-box/)** (HomeProxy/ShellCrash)。
* **我是 Android 用户**: 选 **[Mihomo](./mihomo/)** (FlClash/CMFA) 或 **[Sing-box](./sing-box/)** (官方)。
