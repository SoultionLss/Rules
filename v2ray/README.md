# v2ray 规则集

本目录包含以下策略组的规则文件。

## 策略组列表

### AI

- 合并文件: `AI_domain.txt`
- 独立文件:
  - `Anthropic_domain.txt`
  - `Claude_domain.txt`
  - `xAI_domain.txt`

### ApplePush

- 合并文件: `ApplePush_domain.txt`

### Brokerage

- 合并文件: `Brokerage_domain.txt`

### DIRECT

- 合并文件: `DIRECT_domain.txt`

### GitHub

- 合并文件: `GitHub_domain.txt`

### HongKongBanking

- 合并文件: `HongKongBanking_domain.txt`
- 独立文件:
  - `HSBC_HK_domain.txt`

### HongKongSocial

- 合并文件: `HongKongSocial_domain.txt`
- 独立文件:
  - `Line_domain.txt`
  - `Whatsapp_domain.txt`

### LowRate

- 合并文件: `LowRate_domain.txt`

### Social

- 合并文件: `Social_domain.txt`
- 独立文件:
  - `Reddit_domain.txt`
  - `Threads_domain.txt`
  - `Twitter_domain.txt`

### Streaming

- 合并文件: `Streaming_domain.txt`
- 独立文件:
  - `Crunchyroll_domain.txt`

## 使用方式
在客户端配置中按需引用对应文件，推荐顺序：独立文件优先，合并文件兜底。

## 更新频率
本规则集每日自动更新（北京时间 20:00）。