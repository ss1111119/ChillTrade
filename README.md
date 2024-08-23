# ChillTrade
專案名稱：幫我下決定：是否可以賣了

這個專案是一個基於Python的工具，專為分析股票表現而設計，幫助你決定是否該賣出手中的股票。工具結合了技術指標、財務比率和AI見解，讓你能夠輕鬆做出明智的投資決策。

專案動機
由於股票市場中的指標繁多且複雜，很多投資者可能會感到困惑，不知道該如何正確地分析個股的表現。這個專案是因為我自己在投資過程中也遇到了類似的困難，因此，我希望藉由AI解讀的方式，幫助自己更好地分析個股，進而做出是否賣出股票的決策，避免持續虧損。

功能特點：

股價分析： 實時分析當前股價與購買價格之間的變化，並計算最大回撤和年化回報率。
技術指標： 包含RSI、MACD、KD指標、布林帶、Ichimoku雲圖等多種技術指標的計算與分析。
財務比率： 分析公司基本面的財務比率，如淨利潤率、股東權益回報率（ROE）和自由現金流。
綜合信號： 根據技術分析和基本面評估，生成綜合信號，幫助決策買入或賣出。
使用建議：

若當前持有該股票，建議根據技術和財務分析的結果進行止損操作。
若尚未持有該股票，建議在觀察市場和公司表現後再做決定。
注意事項：

本工具僅供參考，不構成投資建議。投資有風險，請在投資前做好充分的研究。

---

# 使用說明

## 簡介

**幫我下決定：是否可以賣了** 是一個基於Python的Jupyter Notebook工具，專為分析台灣股票市場（TWSE）的股票表現而設計。該工具使用多種技術指標和財務比率，結合AI見解，幫助你決定是否該賣出手中的股票。

## 系統需求

- Jupyter Notebook
- Python 3.8 及以上版本
- 需要安裝以下Python庫：
  - `yfinance`
  - `pandas`
  - `talib`
  - `google-generativeai`
  - 其他依賴可在`requirements.txt`中找到

## 安裝步驟

1. 下載或克隆此專案至本地：

   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   ```

2. 創建虛擬環境（可選）：

   ```bash
   python3 -m venv env
   source env/bin/activate  # 對於Windows系統，請使用 `env\Scripts\activate`
   ```

3. 安裝所需依賴：

   ```bash
   pip install -r requirements.txt
   ```

4. 啟動Jupyter Notebook：

   ```bash
   jupyter notebook
   ```

5. 配置Gemini API Key：

   - 在Notebook中，找到相關代碼行，將你的Gemini API Key替換到 `api_key = ''` 這行。
   - 如果沒有Google Gemini API Key，請至Google Cloud Console進行申請。

## 使用方法

1. 編輯Notebook中的 `ticker` 和 `buy_price` 參數：

   - `ticker` 是你想分析的台股代碼，例如：`2408.TW`。
   - `buy_price` 是你的購買價格，用於計算回報率和止損策略。

2. 按順序運行Notebook中的每個Cell：

   - 使用 `Shift + Enter` 執行每個Cell，Notebook會逐步生成分析結果。

3. 查看分析結果：

   - Notebook的輸出區域將會顯示一份詳細的股票分析報告，包含技術指標、財務比率、綜合信號以及AI生成的投資建議。
   - 你可以根據這些信息做出賣出或持有的決定。

## 常見問題

### 如何替換台股代碼？

在Notebook中找到 `ticker = '2408.TW'`，將 `'2408.TW'` 替換為你想分析的其他股票代碼，例如 `'2330.TW'` 代表台積電。

### 如果分析結果不完整或出錯？

請確保你已經安裝了所有依賴項，並且API Key已正確配置。如果問題依然存在，可以通過 `print` 調試信息來排查具體問題。

### 怎麼處理「無法獲取股東信息」的錯誤？

此錯誤可能是由於API限制或股票數據不足導致的。你可以忽略此錯誤，因為這不會影響主要的技術分析結果。

## 版權與許可
