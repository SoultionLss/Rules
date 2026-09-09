# Surge 规则集

本目录包含 Surge 平台的规则文件和主配置文件。

## 📁 目录结构

```
Surge/
├── 策略组目录/          # 每个策略组一个子目录
│   ├── 合集文件          # 合并后的规则文件 (.list)
│   └── 独立文件          # 独立规则源文件 ({ext})
└── Surge.conf          # 主配置文件
```

## 📋 策略组列表

### AI

- **合集** `AI`：包含 Anthropic, Claude, OpenAI
- **独立** `OpenAI`
- **独立** `Claude`
- **独立** `Anthropic`

### ApplePush

- **独立** `ApplePush`

### Brokerage

- **合集** `Brokerage`：包含 Broker
- **独立** `Broker`

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
- **独立** `GitHub`
- **独立** `GitLab`
- **独立** `Atlassian`
- **独立** `Cloudflare`

### Google

- **合集** `Google`：包含 Gemini, Google
- **独立** `Google`
- **独立** `Gemini`

### HongKongBanking

- **合集** `HongKongBanking`：包含 HKBank, HK_Banks_Direct, HSBC_HK
- **独立** `HSBC_HK`
- **独立** `HK_Banks_Direct`
- **独立** `HKBank`

### HongKongSocial

- **合集** `HongKongSocial`：包含 Line, Whatsapp
- **独立** `Whatsapp`
- **独立** `Line`

### LowRate

- **合集** `LowRate`：包含 PikPak, TeraBox
- **独立** `PikPak`
- **独立** `TeraBox`

### Microsoft

- **合集** `Microsoft`：包含 Microsoft
- **独立** `Microsoft`

### REJECT

- **合集** `REJECT`：包含 BlockHttpDNS
- **独立** `BlockHttpDNS`

### Social

- **合集** `Social`：包含 Instagram, Reddit, Threads, Twitter
- **独立** `Twitter`
- **独立** `Instagram`
- **独立** `Threads`
- **独立** `Reddit`

### Streaming

- **合集** `Streaming`：包含 Crunchyroll, Disney, HBO, Hulu, Netflix, Peacock, PrimeVideo
- **独立** `Netflix`
- **独立** `Disney`
- **独立** `HBO`
- **独立** `PrimeVideo`
- **独立** `Hulu`
- **独立** `Peacock`
- **独立** `Crunchyroll`

### Telegram

- **合集** `Telegram`：包含 Telegram
- **独立** `Telegram`

### TikTok

- **合集** `TikTok`：包含 TikTok
- **独立** `TikTok`

### YouTube

- **合集** `YouTube`：包含 YouTube
- **独立** `YouTube`
## 🔗 引用示例

### 单条规则引用

```surge
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Surge/AI/AI.list, AI
```

### 完整配置示例

```surge
[Rule]
# 合并源: OpenAI, Claude, Grok (共 3 个源)
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Surge/AI/AI.list, AI
# 独立源
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Surge/Google/Google.list, Google
FINAL, PROXY
```

### 官方文档

更多语法请参考: https://manual.nssurge.com/book/understanding-surge/rules/rule-set.html

## 📅 更新频率

本规则集每日自动更新（北京时间 20:00）。

---

*最后更新: 2026-09-09 15:33:34*