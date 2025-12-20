# 📦 混合/高性能框架 (Hybrid / eBPF)

> **简介**: 这类工具通常不局限于单一内核，或者采用 eBPF 等底层技术绕过传统的 TUN/TAP 机制，以追求极致的性能或全能的兼容性。

## 🐧 Linux (eBPF 高性能路由)

### dae (eBPF)
* **核心**: 基于 eBPF 技术。
* **优势**:
    * **极致性能**: 绕过传统协议栈，性能损耗极低，几乎不占用 CPU。
    * **透明代理**: 对 Linux 作为网关（软路由）的场景极度友好。
* **缺点**: 配置门槛极高，容错率低。

### daed (dae dashboard)
* **核心**: dae 的 Web 管理面板。
* **优势**: 让 dae 的配置可视化，降低了使用门槛。
* **评价**: Linux 软路由玩家追求极致性能的首选方案之一。

## 🤖 Android (Root 框架)

### Box for Root (BFR) / Box4Magisk
* **类型**: Magisk / KernelSU / APatch 模块。
* **核心**: **全家桶** (集成 Mihomo, Sing-box, V2ray, Xray 等所有核心)。
* **优势**:
    * **无感代理**: 通过 Root 权限接管系统底层网络，不论 App 怎么检测代理都能生效。
    * **灵活性**: 可以在不同核心之间随意切换。
* **缺点**: 需要手机 Root，有变砖或银行 App 无法使用的风险。

## 🛗 OpenWrt (多核心聚合)

### PassWall
* **核心**: 模块化设计，支持 Xray, Sing-box, Trojan, Hysteria2 等几乎所有核心。
* **评价**: OpenWrt 上最强大的“瑞士军刀”，什么协议出来它都能第一时间挂载对应的二进制文件来支持。
