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

*最后更新: 2026-09-09 14:54:18*