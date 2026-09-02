# v2ray 规则集

本目录包含 v2ray 平台的规则文件和主配置文件。

## 📁 目录结构

```
v2ray/
├── 策略组目录/          # 每个策略组一个子目录
│   ├── 合集文件          # 合并后的规则文件
│   └── 独立文件          # 独立规则源文件
└── v2ray.conf     # 主配置文件
```

## 📋 策略组列表

### AI

- **合集** `AI`：包含 Anthropic, Claude, OpenAI, xAI

### AppleDirect

- **独立** `apple`

### ApplePush

- **独立** `ApplePush`

### BiliBili

- **独立** `BiliBili`

### Brokerage

- **合集** `Brokerage`：包含 Broker

### ChinaCIDR

- **独立** `ChinaCIDR`
- **独立** `cn`

### ChinaMax

- **独立** `ChinaMax`

### DIRECT

- **独立** `DouYin`

### GitHub

- **合集** `GitHub`：包含 Atlassian, Cloudflare, GitHub, GitLab

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

### SOOP

- **独立** `Soop`

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

### v2ray
```
# 在 v2ray.conf 中引用规则文件
RULE-SET, https://raw.githubusercontent.com/SoultionLss/Rules/main/v2ray/AI/AI_domain.txt, AI
RULE-SET, https://raw.githubusercontent.com/SoultionLss/Rules/main/v2ray/Google/Google_domain.txt, Google
```

### CDN 加速（jsDelivr）
```
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/v2ray/AI/AI_domain.txt, AI
```

## 📅 更新频率

本规则集每日自动更新（北京时间 20:00）。

---

*最后更新: 2026-09-02 14:29:11*