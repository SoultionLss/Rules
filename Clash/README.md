# Clash 规则集

本目录包含 Clash 平台的规则文件和主配置文件。

## 📁 目录结构

```
Clash/
├── 策略组目录/          # 每个策略组一个子目录
│   ├── 合集文件          # 合并后的规则文件 (.yaml)
│   └── 独立文件          # 独立规则源文件 ({ext})
└── Clash.yaml          # 主配置文件
```

## 📋 策略组列表

### AI

- **合集** `AI`：包含 Anthropic, Claude, OpenAI

### ApplePush

- **独立** `ApplePush`

### Brokerage

- **合集** `Brokerage`：包含 Broker

### DIRECT

- **独立** `DouYin`
- **独立** `BiliBili`
- **独立** `apple`
- **独立** `Soop`
- **独立** `cn`
- **独立** `ChinaMax`
- **独立** `ChinaCIDR`

### GitHub

- **合集** `GitHub`：包含 Atlassian, GitHub, GitLab
- **独立** `Cloudflare`

### Google

- **合集** `Google`：包含 Gemini, Google

### HongKongBanking

- **合集** `HongKongBanking`：包含 HKBank, HK_Banks_Direct, HSBC_HK

### HongKongSocial

- **合集** `HongKongSocial`：包含 Line, Whatsapp

### LowRate

- **合集** `LowRate`：包含 PikPak, TeraBox

### Microsoft

- **合集** `Microsoft`：包含 Microsoft

### REJECT

- **合集** `REJECT`：包含 BlockHttpDNS

### Social

- **合集** `Social`：包含 Instagram, Reddit, Threads, Twitter

### Streaming

- **合集** `Streaming`：包含 Crunchyroll, Disney, HBO, Hulu, Netflix, Peacock, PrimeVideo

### Telegram

- **合集** `Telegram`：包含 Telegram

### TikTok

- **合集** `TikTok`：包含 TikTok

### YouTube

- **合集** `YouTube`：包含 YouTube
## 🔗 引用示例

### 单条规则引用

```clash
rule-providers:
  AI:
    type: http
    url: https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Clash/AI/AI.yaml
    interval: 86400
    behavior: classical
rules:
  - RULE-SET, AI, AI
```

### 完整配置示例

```clash
rule-providers:
  AI:
    type: http
    url: https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Clash/AI/AI.yaml
    interval: 86400
    behavior: classical
  Google:
    type: http
    url: https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Clash/Google/Google.yaml
    interval: 86400
    behavior: classical
rules:
  # 合并源: OpenAI, Claude, Grok (共 3 个源)
  - RULE-SET, AI, AI
  # 独立源
  - RULE-SET, Google, Google
  - MATCH, PROXY
```

### 官方文档

更多语法请参考: https://clashfaq.com/rule-providers/

## 📅 更新频率

本规则集每日自动更新（北京时间 20:00）。

---

*最后更新: 2026-09-02 18:29:26*