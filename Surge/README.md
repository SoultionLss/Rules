# Surge 规则集

本目录包含以下策略组的规则文件。

## 策略组列表

### AI

- 合并文件: `AI.list`
- 独立文件:
  - `Anthropic.list`
  - `Claude.list`
  - `xAI.list`

### ApplePush

- 合并文件: `ApplePush.list`

### Brokerage

- 合并文件: `Brokerage.list`

### DIRECT

- 合并文件: `DIRECT.list`

### GitHub

- 合并文件: `GitHub.list`

### HongKongBanking

- 合并文件: `HongKongBanking.list`
- 独立文件:
  - `HSBC_HK.list`

### HongKongSocial

- 合并文件: `HongKongSocial.list`
- 独立文件:
  - `Line.list`
  - `Whatsapp.list`

### LowRate

- 合并文件: `LowRate.list`

### Social

- 合并文件: `Social.list`
- 独立文件:
  - `Reddit.list`
  - `Threads.list`
  - `Twitter.list`

### Streaming

- 合并文件: `Streaming.list`
- 独立文件:
  - `Crunchyroll.list`

## 使用方式
在客户端配置中按需引用对应文件，推荐顺序：独立文件优先，合并文件兜底。

## 更新频率
本规则集每日自动更新（北京时间 20:00）。