```markdown
# Rules · 多平台分流规则集

[![GitHub Actions](https://img.shields.io/badge/Actions-自动构建-blue?logo=github)](https://github.com/SoultionLss/MyRules/actions)
[![License](https://img.shields.io/badge/License-MIT-green)](#)

本仓库由 **[MyRules](https://github.com/SoultionLss/MyRules)** 自动化流水线生成，每日聚合多个公开规则源，生成适配 **7 个主流代理客户端** 的规则文件和配置文件，开箱即用。
个人自用仓库
---
```
## ✨ 特性

- 🔄 **每日自动更新**：北京时间 20:00 自动拉取上游最新规则
- 🧩 **多源聚合**：整合 blackmatrix7、Loyalsoldier、ACL4SSR 等主流规则源
- 📦 **7 平台支持**：Surge、Clash、Egern、Loon、Quantumult X、Sing-box、v2ray
- ⚙️ **智能合并**：同类规则（如 AI、流媒体）自动合并为合集，减少配置冗余
- 🚀 **CDN 加速**：所有规则文件通过 jsDelivr CDN 分发，加载速度快

---

## 📂 目录结构

```markdown
Rules/
├── Surge/                     # Surge 平台
│   ├── AI/                    # AI 服务合集
│   │   ├── AI.list            # 合集文件（OpenAI + Claude + Anthropic + Grok）
│   │   ├── OpenAI.list        # 独立源
│   │   ├── Claude.list        # 独立源
│   │   └── Anthropic.list     # 独立源
│   ├── Google/                # Google 服务合集
│   │   └── Google.list
│   ├── Streaming/             # 流媒体合集
│   │   ├── Streaming.list
│   │   ├── Netflix.list
│   │   ├── Disney.list
│   │   └── ...
│   ├── Social/                # 社交媒体合集
│   ├── DIRECT/                # 国内直连
│   ├── REJECT/                # 广告拦截
│   └── Surge.conf             # Surge 主配置文件
├── Clash/                     # Clash / Mihomo 平台
│   ├── AI/
│   │   ├── AI.yaml
│   │   └── ...
│   ├── Google/
│   │   └── Google.yaml
│   └── Clash.yaml             # Clash 主配置文件
├── Egern/                     # Egern 平台
│   ├── AI/
│   │   ├── AI.yaml
│   │   └── ...
│   └── Egern.yaml             # Egern 主配置文件
├── Loon/                      # Loon 平台
│   ├── AI/
│   │   ├── AI.list
│   │   └── ...
│   └── Loon.conf              # Loon 主配置文件
├── QuantumultX/               # Quantumult X 平台
│   ├── AI/
│   │   ├── AI.list
│   │   └── ...
│   └── QuantumultX.conf       # Quantumult X 主配置文件
├── Singbox/                   # Sing-box 平台
│   ├── AI/
│   │   ├── AI.json
│   │   └── ...
│   └── Singbox.json           # Sing-box 主配置文件
└── v2ray/                     # v2ray / Xray 平台
    ├── AI/
    │   ├── AI_domain.txt
    │   └── ...
    └── v2ray.json             # v2ray 主配置文件
```

---

## 🚀 快速开始

### 1. 直接引用主配置文件（推荐）

每个平台根目录下都提供了完整的主配置文件，可直接导入客户端使用：

| 平台 | 主配置文件 | CDN 加速链接 |
|------|-----------|-------------|
| **Surge** | `Surge/Surge.conf` | `https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Surge/Surge.conf` |
| **Clash** | `Clash/Clash.yaml` | `https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Clash/Clash.yaml` |
| **Egern** | `Egern/Egern.yaml` | `https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Egern/Egern.yaml` |
| **Loon** | `Loon/Loon.conf` | `https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Loon/Loon.conf` |
| **Quantumult X** | `QuantumultX/QuantumultX.conf` | `https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/QuantumultX/QuantumultX.conf` |
| **Sing-box** | `Singbox/Singbox.json` | `https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Singbox/Singbox.json` |
| **v2ray** | `v2ray/v2ray.json` | `https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/v2ray/v2ray.json` |

### 2. 引用单个策略组规则

如果需要单独引用某个策略组的规则文件，可使用以下格式：

**Surge / Loon / Quantumult X（`.list` 格式）**
```list
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Surge/AI/AI.list, AI
```

**Clash / Egern（`.yaml` 格式）**
```yaml
# Clash
- RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Clash/AI/AI.yaml, AI

# Egern
- rule_set:
    match: https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Egern/AI/AI.yaml
    policy: AI
```

**Sing-box（`.json` 格式）**
```json
{
  "route": {
    "rule_set": [{
      "tag": "AI",
      "type": "remote",
      "format": "source",
      "url": "https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Singbox/AI/AI.json"
    }],
    "rules": [{ "rule_set": "AI" }]
  }
}
```

**v2ray（`_domain.txt` 格式）**
```json
{
  "routing": {
    "rules": [
      { "domain": ["geosite:AI"] }
    ]
  }
}
```

---

## 📋 策略组说明

| 策略组 | 说明 | 包含的规则源 |
|--------|------|-------------|
| **AI** | AI 服务合集 | OpenAI、Claude、Anthropic、Grok 等 |
| **Google** | Google 全系列服务 | Google、Gemini |
| **Streaming** | 流媒体服务合集 | Netflix、Disney+、HBO、PrimeVideo、Hulu、Peacock、Crunchyroll |
| **Social** | 社交媒体合集 | Twitter、Instagram、Threads、Reddit |
| **YouTube** | YouTube 视频及 API | YouTube |
| **GitHub** | 代码托管合集 | GitHub、GitLab、Atlassian、Cloudflare |
| **Telegram** | Telegram 消息服务 | Telegram |
| **Microsoft** | 微软服务合集 | Microsoft（bing.cn 直连） |
| **HongKongSocial** | 香港社交合集 | WhatsApp、Line |
| **HongKongBanking** | 香港银行合集 | 汇丰、中银、恒生、众安等 |
| **Brokerage** | 券商服务合集 | 富途、长桥、老虎、嘉信等 |
| **ApplePush** | Apple 推送服务 | Apple 推送通知 |
| **AppleDirect** | Apple 服务直连 | iCloud、App Store 等 |
| **LowRate** | 低倍率节点合集 | PikPak、Terabox |
| **DIRECT** | 国内直连 | 抖音、哔哩哔哩、局域网、ChinaMax、GeoIP CN 等 |
| **REJECT** | 广告拦截 | HTTPDNS、广告规则等 |
| **SOOP** | SOOP 直播直连 | SOOP |
| **BiliBili** | 哔哩哔哩直连 | BiliBili |
| **ChinaMax** | 国内服务直连 | ChinaMax |
| **ChinaCIDR** | 中国 IP 段直连 | ChinaCIDR、GeoIP CN |

> 💡 **合并规则说明**：部分策略组（如 AI、Streaming）包含多个规则源，它们会被合并到一个文件中。在主配置文件中，合集文件引用上方会显示 `# 合并源: xxx, xxx (共 N 个源)` 注释，方便你了解该文件包含哪些子源。

---

## 📝 规则来源

本项目聚合了以下主流规则源：

| 来源 | 说明 |
|------|------|
| [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script) | 最全的 iOS/Clash 规则集 |
| [Loyalsoldier/surge-rules](https://github.com/Loyalsoldier/surge-rules) | 精简域名规则 |
| [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip) | GeoIP 国家 IP 段 |
| [ACL4SSR/ACL4SSR](https://github.com/ACL4SSR/ACL4SSR) | 广告拦截规则 |
| [Repcz/Tool](https://github.com/Repcz/Tool) | Egern 规则集 |
| [Accademia/Additional_Rule_For_Clash](https://github.com/Accademia/Additional_Rule_For_Clash) | 香港银行、国内直连 |
| [forecho/broker-rules](https://github.com/forecho/broker-rules) | 券商分流规则 |
| [Rabbit-Spec/Surge](https://github.com/Rabbit-Spec/Surge) | ChinaCIDR 直连 |
| [LingJingMaster/Shadowrocket-Rules](https://github.com/LingJingMaster/Shadowrocket-Rules) | 香港银行、苹果推送 |
| [MetaCubeX/meta-rules-dat](https://github.com/MetaCubeX/meta-rules-dat) | GeoIP / GeoSite / ASN 规则 |

---

## 📅 更新频率

- **自动更新**：每天北京时间 20:00（UTC 12:00）自动拉取上游规则并重新生成
- **更新内容**：
  - 上游规则源更新 → 自动同步
  - 规则源配置变更 → 自动重新生成
  - 新增策略组 → 自动生成对应目录和文件

---

## 🔗 相关链接

| 项目 | 链接 |
|------|------|
| **规则仓库（本仓库）** | [SoultionLss/Rules](https://github.com/SoultionLss/Rules) |
| **CDN 加速** | [jsDelivr](https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/) |

---

## 📄 许可证

[MIT License](https://opensource.org/licenses/MIT)

---

*最后更新: 2026-09-02*
