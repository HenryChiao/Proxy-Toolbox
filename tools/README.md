# 🧰 小工具 (Toolkit)

> **简介**: 这些工具主要用于对订阅、规则和脚本进行更高级的管理和转换，适合进阶用户。

## 1. 订阅与规则管理

### Sub-Store
* **功能**: 搭建私人的订阅管理库。支持对订阅节点进行筛选、重命名、组合等高级操作，生成新的订阅链接。
* **部署环境**:
    * Node.js
    * Docker (`xream/sub-store:latest`)
* **关联**: 许多高级用户使用它来清洗机场订阅，再导入到 Surge/Clash/Loon 中。

### SubCase 🆕
* **关联**: 🤖 Android
* **功能**: **Sub-Store** 的 Android APK 封装版。
* **亮点**: 无需 Root 即可在安卓手机上运行 Sub-Store 后端，方便移动端用户管理订阅。

---

## 2. 脚本与模块转换

### Script Hub
* **功能**: 专门用于解决 iOS 代理生态中“方言不通”的问题。
* **用途**: 在 **Quantumult X (QX)**、**Surge**、**Loon**、**Stash** 之间转换模块 (Module) 或 覆写 (Rewrite) 规则。
* **部署环境**:
    * Node.js
    * Docker (`xream/script-hub:latest`)
    * [在线版链接](../converters/README.md)
