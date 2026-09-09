# v2ray 规则集

本目录包含 v2ray 平台的规则文件和主配置文件。

## 📁 目录结构

```
v2ray/
├── 策略组目录/          # 每个策略组一个子目录
│   ├── 合集文件          # 合并后的规则文件 (_domain.txt)
│   └── 独立文件          # 独立规则源文件 ({ext})
└── v2ray.json          # 主配置文件
```

## 📋 策略组列表

## 🔗 引用示例

### 单条规则引用

```v2ray
{
  "routing": {
    "rules": [
      { "domain": ["geosite:AI"] }
    ]
  }
}
```

### 完整配置示例

```v2ray
{
  "routing": {
    "rules": [
      { "domain": ["geosite:AI"] },
      { "domain": ["geosite:Google"] }
    ]
  }
}
```

### 官方文档

更多语法请参考: https://www.v2fly.org/config/routing.html#ruleobject

## 📅 更新频率

本规则集每日自动更新（北京时间 20:00）。

---

*最后更新: 2026-09-09 14:54:18*