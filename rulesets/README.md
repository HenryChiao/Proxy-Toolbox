# 📒 规则集 (Rulesets)

> **简介**: 优质的规则集是分流策略的基石。本文档汇总了各大主流内核（Mihomo, Sing-box）及 iOS 代理软件的常用规则源。

## 1. GeoIP / GeoSite (通用基础规则)

这类规则集主要包含 IP 段（GeoIP）和 域名列表（GeoSite），是判断流量“出国”还是“回国”的基础。

| 维护者/仓库 | 格式 | 备注 |
| :--- | :--- | :--- |
| **Loyalsoldier/v2ray-rules-dat** 🔥 | `dat` | 老字号源，许多第三方规则的上游。 |
| **MetaCubeX/meta-rules-dat** | `dat` | Mihomo/MetaCubeX 官方维护，合并自 Loyalsoldier 等。 |
| **苍狼山庄 运营商IP段** | `txt`, `html` | 细分 ISP (电信/联通/移动/教育网等)及港澳台 IP。 |
| **CHIZI-0618/v2ray-rules-dat** 🔴 | `dat` | 已断更。 |

---

## 2. Mihomo / Stash / Clash 专用规则

> **💡 性能提示**: 在匹配效率上，**二进制 (`mrs`) ＞ 文本 (`yaml`/`list`)**。建议优先采用 `mrs` 规则。
> *注: Stash 3.1.1 (2025年6月) 及之后的版本才支持 `mrs` 规则。*

| 维护者/仓库 | 格式 | 说明 |
| :--- | :--- | :--- |
| **MetaCubeX/meta-rules-dat** 🧑‍💼 | `mrs`, `dat`, `yaml`, `list` | **官方维护**。从 Loyalsoldier、CHIZI 等上游合并。 |
| **DustinWin/ruleset_geodata** | `mrs`, `yaml`, `list` | 大多为融合规则集，合并自 Loyalsoldier 等。 |
| **blackmatrix7/ios_rule_script** 🔥 | `yaml`, `list` | 知名的第三方规则集。**缺点**: 缺 `mrs` 二进制格式。 |
| **deezertidal/Stash** | - | **Stash 专用** 的覆写规则/模块。 |

---

## 3. Sing-box 专用规则

> **⚠️ 版本警告**: Sing-box 的 rule-set 版本存在迭代。现主流为 **Format Version 3** (适配 Core v1.11.x+)。请注意区分 `srs` (二进制) 版本。

| 维护者/仓库 | 格式 | 说明 |
| :--- | :--- | :--- |
| **SagerNet/sing_geosite** 🧑‍💼 | `srs` (v3), `db` | **官方维护** (域名)。 |
| **SagerNet/sing_geoip** 🧑‍💼 | `srs` (v3), `db` | **官方维护** (IP)。 |
| **MetaCubeX/meta-rules-dat/sing** | `srs` (v2), `json` | 隔壁 MetaCubeX 维护的版本。 |
| **DustinWin/ruleset_geodata** | `srs` (v2~v3), `json` | 融合规则集。 |
| **Senshinya/singbox_ruleset** | `srs` (v2), `json` | 基于 blackmatrix7 的转译版。 |

---

## 4. iOS Apps (Surge / Loon / QX) 专用

| 维护者/仓库 | 适用 App | 说明 |
| :--- | :--- | :--- |
| **blackmatrix7/ios_rule_script** 🔥 | 全平台 | 最知名的第三方规则集，适配各种 App 的文本格式。 |
| **Loon 模块库** | Loon | 官方或社区维护的模块。 |
| **可莉的 Loon 模块** | Loon | 知名模块源。 |
| **Surge 模块库** | Surge | 基于“可莉”的转译版，原生仅适配 Surge。 |
| **松果库 (Egern 模块库)** 🆕 | Egern, Surge, Loon, QX | Egern 开发者(鼠爸)建站。原生适配 Egern，兼容其他。 |
| **whatshub** | - | iOS 覆写规则/模块。 |

---

## 5. ⛔️ 防广告规则集 (Anti-ADs)

> **ℹ️ 提示**: 规则集对现今网页的广告防护有限。**规则集 < MitM 重写 < 浏览器插件 (如 uBlock Origin)**。

| 维护者/项目 | 覆盖范围 | 备注 |
| :--- | :--- | :--- |
| **privacy-protection-tools/anti-AD** 🔥 | 极广 | 适配 AdGuard, Mihomo, Sing-box, Surge 等几乎全平台。 |
| **217heidai/adblockfilters (黑带)** 🔥 | 较广 | 不支持 MosDNS。 |
| **TG-Twilight/AWAvenue-Ads-Rule (秋风)** | 中等 | 不支持 SmartDNS。Sing-box 仅 json，Mihomo 仅 yaml。 |
| **Cats-Team/AdRules** | 较广 | 适配 AdGuard, MosDNS, Clash, Sing-box, QX, Surge 等。 |

