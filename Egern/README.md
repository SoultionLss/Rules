# Egern 规则集

本目录包含 Egern 平台的规则文件和主配置文件。

## 📁 目录结构

```
Egern/
├── 策略组目录/          # 每个策略组一个子目录
│   ├── 合集文件          # 合并后的规则文件 (.yaml)
│   └── 独立文件          # 独立规则源文件 ({ext})
└── Egern.yaml          # 主配置文件
```

## 📋 策略组列表

### AI

- **合集** `OpenAI`：包含 OpenAI
- **合集** `Claude`：包含 Claude
- **合集** `Anthropic`：包含 Anthropic

### ApplePush

- **独立** `ApplePush`

### Brokerage

- **合集** `HKBrokerage`：包含 Broker

### DIRECT

- **合集** `Soop`：包含 Soop
- **独立** `DouYin`
- **独立** `BiliBili`
- **独立** `apple`
- **独立** `cn`
- **独立** `ChinaMax`
- **独立** `ChinaCIDR`

### GitHub

- **合集** `GitHub`：包含 Atlassian, GitHub, GitLab
- **合集** `Cloudflare`：包含 Cloudflare

### Google

- **合集** `Google`：包含 Google
- **合集** `Gemini`：包含 Gemini

### HongKongBanking

- **合集** `HSBC_HK`：包含 HSBC_HK
- **合集** `HK_Banks_Direct`：包含 HK_Banks_Direct
- **合集** `HKBank`：包含 HKBank

### HongKongSocial

- **合集** `Whatsapp`：包含 Whatsapp
- **合集** `Line`：包含 Line

### LowRate

- **合集** `PikPak`：包含 PikPak
- **合集** `TeraBox`：包含 TeraBox

### Microsoft

- **合集** `Microsoft`：包含 Microsoft

### REJECT

- **合集** `REJECT`：包含 BlockHttpDNS

### Social

- **合集** `Twitter`：包含 Twitter
- **合集** `Instagram`：包含 Instagram
- **合集** `Threads`：包含 Threads
- **合集** `Reddit`：包含 Reddit

### Streaming

- **合集** `Netflix`：包含 Netflix
- **合集** `Disney`：包含 Disney
- **合集** `HBO`：包含 HBO
- **合集** `PrimeVideo`：包含 PrimeVideo
- **合集** `Hulu`：包含 Hulu
- **合集** `Peacock`：包含 Peacock
- **合集** `Crunchyroll`：包含 Crunchyroll

### Telegram

- **合集** `Telegram`：包含 Telegram

### TikTok

- **合集** `TikTok`：包含 TikTok

### YouTube

- **合集** `YouTube`：包含 YouTube
## 🔗 引用示例

### 单条规则引用

```egern
- rule_set:
    match: https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Egern/AI/AI.yaml
    policy: AI
```

### 完整配置示例

```egern
rules:
  # 合并源: OpenAI, Claude, Grok (共 3 个源)
  - rule_set:
      match: https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Egern/AI/AI.yaml
      policy: AI
  # 独立源
  - rule_set:
      match: https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Egern/Google/Google.yaml
      policy: Google
  - default:
      policy: PROXY
```

### 官方文档

更多语法请参考: https://egernapp.com/docs/

## 📅 更新频率

本规则集每日自动更新（北京时间 20:00）。

---

*最后更新: 2026-09-09 15:16:15*