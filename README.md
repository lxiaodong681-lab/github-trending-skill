# GitHub Trending Skill

每日抓取 GitHub Trending 热榜，支持日榜和月度汇总。

## 功能

- daily: 今日热榜摘要
- monthly: 过去 30 天综合热度 Top 10

## 依赖

- Python 3.8+
- requests
- beautifulsoup4

## 使用方式

### CLI 运行

```bash
python scripts\run.py --mode daily --language All --limit 10
python scripts\run.py --mode monthly --language All --limit 10
```

### 作为脚本导入

```python
from scripts.daily import run as run_daily
from scripts.monthly import run as run_monthly

print(run_daily(language="Python", limit=5))
print(run_monthly(language="All", limit=10))
```

## 说明

- 月度模式会按语言循环抓取，并且每次请求之间至少等待 3 秒。
- 若网络失败且存在缓存，将返回缓存结果并附带提示。
- 所有时间戳均为 UTC。

## 调度建议

- mode=daily: 每天 UTC 08:00
- mode=monthly: 每月 1 日 UTC 00:00

