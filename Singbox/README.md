# Singbox 规则集

本目录包含以下策略组的规则文件。

## 策略组列表

### AI

- 合并文件: `AI.json`
- 独立文件:
  - `Anthropic.json`
  - `Claude.json`
  - `xAI.json`

### ApplePush

- 合并文件: `ApplePush.json`

### Brokerage

- 合并文件: `Brokerage.json`

### DIRECT

- 合并文件: `DIRECT.json`

### GitHub

- 合并文件: `GitHub.json`

### HongKongBanking

- 合并文件: `HongKongBanking.json`
- 独立文件:
  - `HSBC_HK.json`

### HongKongSocial

- 合并文件: `HongKongSocial.json`
- 独立文件:
  - `Line.json`
  - `Whatsapp.json`

### LowRate

- 合并文件: `LowRate.json`

### Social

- 合并文件: `Social.json`
- 独立文件:
  - `Reddit.json`
  - `Threads.json`
  - `Twitter.json`

### Streaming

- 合并文件: `Streaming.json`
- 独立文件:
  - `Crunchyroll.json`

## 使用方式
在客户端配置中按需引用对应文件，推荐顺序：独立文件优先，合并文件兜底。

## 更新频率
本规则集每日自动更新（北京时间 20:00）。