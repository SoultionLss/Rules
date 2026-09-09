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

*最后更新: 2026-09-09 14:54:18*