# 香港市場廣度監測（Stockbee Market Monitor 香港版）

仿照 jp-breadth 的做法：港交所主板 + GEM 普通股，Yahoo Finance 日線（約 3 年），
每日計算 4% 漲跌家數、5/10 日比率、季度/月度 ±25%、月度 ±50%、34 日 ±13%、T2108，
另有 52 週新高/新低頁（highs.html）。

- 股票池：HKEX List of Securities → Category=Equity，Sub-Category=Main Board/GEM，港幣櫃台，代號 < 10000，排除優先股
- 流動性過濾：20 日平均成交金額 ≥ HK$500,000（約等於日本版 ¥1,000 萬）
- 對照指數：^HSI、2800.HK（盈富基金）

每日更新（香港/台北時間 17:00 之後）：`bash scripts/update_all.sh`
