# Singbox 规则集

本目录包含 Singbox 平台的规则文件和主配置文件。

## 📁 目录结构

```
Singbox/
├── 策略组目录/          # 每个策略组一个子目录
│   ├── 合集文件          # 合并后的规则文件 (.json)
│   └── 独立文件          # 独立规则源文件 ({ext})
└── Singbox.json          # 主配置文件
```

## 📋 策略组列表

## 🔗 引用示例

### 单条规则引用

```singbox
{
  "route": {
    "rule_set": [
      {
        "tag": "AI",
        "type": "remote",
        "format": "source",
        "url": "https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Singbox/AI/AI.json"
      }
    ],
    "rules": [
      { "rule_set": "AI" }
    ]
  }
}
```

### 完整配置示例

```singbox
{
  "route": {
    "rule_set": [
      {
        "tag": "AI",
        "type": "remote",
        "format": "source",
        "url": "https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Singbox/AI/AI.json"
      },
      {
        "tag": "Google",
        "type": "remote",
        "format": "source",
        "url": "https://cdn.jsdelivr.net/gh/SoultionLss/Rules@main/Singbox/Google/Google.json"
      }
    ],
    "rules": [
      { "rule_set": "AI" },
      { "rule_set": "Google" }
    ]
  }
}
```

### 官方文档

更多语法请参考: https://sing-box.sagernet.org/configuration/route/rule-set/

## 📅 更新频率

本规则集每日自动更新（北京时间 20:00）。

---

*最后更新: 2026-09-09 14:54:18*