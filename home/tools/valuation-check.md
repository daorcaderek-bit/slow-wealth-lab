# 估值查询

## 各资产估值数据源

### 美股（S&P 500）

| 指标 | 网站 | 当前怎么看 |
|------|------|-----------|
| CAPE（席勒市盈率） | multpl.com/shiller-pe | 首页直接显示当前值 |
| Trailing PE | multpl.com/s-p-500-pe-ratio | 首页直接显示 |
| Forward PE | yardeni.com | 研报中查找 |

**CAPE 估值参考：**
- < 15：极度低估（历史级别买入机会）
- 15-20：低估
- 20-25：正常
- 25-30：偏高
- 30+：高估（当前区域）

### A股

| 指标 | 网站 |
|------|------|
| 沪深300 PE/PB/百分位 | legulegu.com |
| 中证红利 股息率 | 中证指数官网 csindex.com.cn |
| 综合估值 | 蛋卷基金 danjuanfunds.com |

### 加密

| 指标 | 网站 |
|------|------|
| Fear & Greed Index | alternative.me/crypto/fear-and-greed-index |
| BTC 彩虹图 | blockchaincenter.net/bitcoin-rainbow-chart |
| BTC 链上指标 | lookintobitcoin.com |

## 怎么读估值

| 百分位 | 含义 | 操作建议 |
|--------|------|---------|
| 0-20% | 低估 | 加大定投（1.4x - 2.0x） |
| 20-50% | 正常偏低 | 正常定投（1.0x - 1.4x） |
| 50-80% | 正常偏高 | 减少定投（0.4x - 0.8x） |
| 80-100% | 高估 | 最低定投（0.2x - 0.3x） |

## 自动化方案

我们建了一个每日自动获取估值的机器人，数据源包括：
- multpl.com（CAPE + PE）
- msci.com（Forward PE）
- 蛋卷基金 API（A股指数）
- alternative.me（加密 F&G）

每天早上自动推送到群里，不需要手动查。
