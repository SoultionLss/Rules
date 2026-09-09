# QuantumultX 规则集

本目录包含 QuantumultX 平台的规则文件和主配置文件。

## 📁 目录结构

```
QuantumultX/
├── 策略组目录/          # 每个策略组一个子目录
│   ├── 合集文件          # 合并后的规则文件 (.list)
│   └── 独立文件          # 独立规则源文件 ({ext})
└── QuantumultX.conf          # 主配置文件
```

## 📋 策略组列表

## 🔗 引用示例

### 单条规则引用

```quantumultx
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/QuantumultX/AI/AI.list, AI
```

### 完整配置示例

```quantumultx
[Rule]
# 合并源: OpenAI, Claude, Grok (共 3 个源)
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/QuantumultX/AI/AI.list, AI
# 独立源
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/QuantumultX/Google/Google.list, Google
FINAL, PROXY
```

### 官方文档

更多语法请参考: https://qx.atlucky.me/rule.html

## 📅 更新频率

本规则集每日自动更新（北京时间 20:00）。

---

*最后更新: 2026-09-09 15:03:06*