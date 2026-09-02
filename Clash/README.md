# Clash 规则集

本目录包含以下策略组的规则文件。

## 策略组列表

### AI

- 合并文件: `AI.yaml`
- 独立文件:
  - `Anthropic.yaml`
  - `Claude.yaml`
  - `xAI.yaml`

### ApplePush

- 合并文件: `ApplePush.yaml`

### Brokerage

- 合并文件: `Brokerage.yaml`

### DIRECT

- 合并文件: `DIRECT.yaml`

### GitHub

- 合并文件: `GitHub.yaml`

### HongKongBanking

- 合并文件: `HongKongBanking.yaml`
- 独立文件:
  - `HSBC_HK.yaml`

### HongKongSocial

- 合并文件: `HongKongSocial.yaml`
- 独立文件:
  - `Line.yaml`
  - `Whatsapp.yaml`

### LowRate

- 合并文件: `LowRate.yaml`

### Social

- 合并文件: `Social.yaml`
- 独立文件:
  - `Reddit.yaml`
  - `Threads.yaml`
  - `Twitter.yaml`

### Streaming

- 合并文件: `Streaming.yaml`
- 独立文件:
  - `Crunchyroll.yaml`

## 使用方式
在客户端配置中按需引用对应文件，推荐顺序：独立文件优先，合并文件兜底。

## 更新频率
本规则集每日自动更新（北京时间 20:00）。