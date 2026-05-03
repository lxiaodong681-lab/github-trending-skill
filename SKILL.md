---
name: github-trending
version: 1.0.0
description: 每日 GitHub Trending 热榜推送，支持日榜和月度汇总
author: 爱好摸鱼真君 & 千绘璃
license: MIT
---

# GitHub Trending

自动抓取 GitHub Trending 热榜，生成中文摘要推送给用户。

## 使用方式

### 每日热榜
mode=daily，默认推送今日最热 10 个仓库

### 月度汇总
mode=monthly，推送上个月综合热度 Top 10

## 参数
- mode: daily | monthly
- language: Python | JavaScript | Go | All（默认 All）
- limit: 数量（默认 10）

