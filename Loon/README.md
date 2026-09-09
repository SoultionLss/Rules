# Loon 规则集

本目录包含 Loon 平台的规则文件和主配置文件。

## 📁 目录结构

```
Loon/
├── 策略组目录/          # 每个策略组一个子目录
│   ├── 合集文件          # 合并后的规则文件 (.list)
│   └── 独立文件          # 独立规则源文件 ({ext})
└── Loon.conf          # 主配置文件
```

## 📋 策略组列表

## 🔗 引用示例

### 单条规则引用

```loon
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Loon/AI/AI.list, AI
```

### 完整配置示例

```loon
[Rule]
# 合并源: OpenAI, Claude, Grok (共 3 个源)
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Loon/AI/AI.list, AI
# 独立源
RULE-SET, https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Loon/Google/Google.list, Google
FINAL, PROXY
```

### 官方文档

更多语法请参考: https://nsloon.app/docs/

## 📅 更新频率

本规则集每日自动更新（北京时间 20:00）。

---

*最后更新: 2026-09-09 15:03:06*