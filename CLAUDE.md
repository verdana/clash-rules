# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 概述

这是 Clash 代理规则仓库，托管在 GitHub (verdana/clash-rules)，包含用于 Clash Verge 的代理规则配置。

## 结构

- `Custom.yaml` - Clash Verge 主配置模板，引用 rule-providers
- `Rules/Common.yaml` - 通用域名规则（社交媒体、开发工具、AI服务、游戏等）
- `Rules/Google.yaml` - Google 全套服务的域名规则

## 规则类型

- `DOMAIN-SUFFIX` - 匹配域名后缀
- `DOMAIN-KEYWORD` - 匹配包含关键字的域名
- `GEOIP` - 基于IP地理位置的规则

## 添加新规则

1. 编辑 `Rules/Common.yaml` 添加通用域名
2. 编辑 `Rules/Google.yaml` 添加 Google 相关域名
3. 提交后推送到 GitHub，Custom.yaml 中的 URL 会自动获取最新规则

## GitHub 仓库

规则通过 jsdelivr CDN 引用：
- Common.yaml: `https://raw.githubusercontent.com/verdana/clash-rules/refs/heads/main/Rules/Common.yaml`
- Google.yaml: `https://raw.githubusercontent.com/verdana/clash-rules/refs/heads/main/Rules/Google.yaml`
