# 智慧健康日誌與風險評估系統 🩺

這是一個基於 Node.js 與 SQLite 開發的 Web 應用程式。使用者可以記錄每日的健康數據（睡眠時數、步數、心情分數），系統會透過整合 **Google Gemini API** 來模擬決策樹邏輯，自動評估並回傳當日的「健康風險等級」（低 / 中 / 高）。

此專案為中原大學之學術展示專案。
**作者：** 塗品妍

## ✨ 核心功能 (Features)

* **📝 完整健康日誌 CRUD：** 支援新增、讀取、修改與刪除使用者的健康紀錄。
* **🤖 AI 風險評估：** 整合 Google Gemini 2.5 Flash 模型，根據輸入特徵即時運算風險等級。
* **🛡️ 防連點與錯誤攔截：** 具備完善的前端按鈕狀態控制，並能精準捕捉 AI API 的 `429 Too Many Requests` (額度上限) 與 `404 Not Found` 錯誤，提供友善的提示。
* **☁️ 雲端部署準備：** 專案架構支援本地端執行，亦可無縫部署至 Render 等雲端平台。

## 🛠️ 技術架構 (Tech Stack)

* **前端：** HTML5, CSS3, Vanilla JavaScript, Fetch API
* **後端：** Node.js, Express.js
* **資料庫：** SQLite3 (本地實體檔案資料庫 `health.db`)
* **外部 API：** Google Gemini AI API (`@google/generative-ai` / `axios`)

## 🚀 快速啟動 (Getting Started)

### 1. 取得專案與安裝依賴
請先將專案 clone 到本地端，並安裝必要的 Node.js 套件：
```bash
git clone [https://github.com/pinyann-1124/123.git](https://github.com/pinyann-1124/123.git)
cd 123
npm install
