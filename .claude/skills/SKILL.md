---
name: clash-rules-patterns
description: Coding patterns from clash-rules repository
version: 1.0.0
source: local-git-analysis
analyzed_commits: 26
---

# Clash Rules Patterns

## Commit Conventions

使用 **conventional commits** 格式：
- `feat(rules): <描述>` - 添加新域名规则
- `[chore]` - 仓库初始化
- `Update YYYYMM` - 月度更新

## 规则格式

YAML 文件中使用两种规则类型：

```yaml
- DOMAIN-SUFFIX,example.com        # 匹配域名后缀
- DOMAIN-KEYWORD,keyword            # 匹配包含关键字的域名
```

## 文件结构

```
.
├── Custom.yaml          # Clash Verge 主配置模板
└── Rules/
    ├── Common.yaml      # 通用域名规则（分类组织）
    └── Google.yaml      # Google 服务域名规则
```

## 添加新域名流程

1. 确定域名类型（通用/Google）
2. 编辑对应 YAML 文件
3. 使用 `git add` 暂存更改
4. 提交格式：`feat(rules): 添加 example.com 域名支持`
5. 推送到 GitHub

## 规则组织

Common.yaml 按类别分组注释：
- 通用站点（社交、云服务）
- Development/Geek/AI（开发工具、AI服务）
- Game（游戏相关）
- nycvod（其他）
