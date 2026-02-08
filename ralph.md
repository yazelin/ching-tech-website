# Task: 重做擎添工業官網

## 目標
將現有的 ching-tech-website 完全重寫，以 https://ching-tech.ddns.net 的內容為基礎，提升設計品質。

## 技術要求
- 純 HTML + CSS + vanilla JS（不用框架）
- 單頁式設計（index.html），所有 section 用錨點導航
- Font Awesome 6.4（CDN）for icons
- Google Fonts: Noto Sans TC + Inter + Space Grotesk
- RWD 響應式，手機優先
- 部署在 GitHub Pages（已有 repo）

## 設計風格
暗色科技風「智慧脈動」：
- 背景：#0A1628（深海藍黑）
- 強調色：#00D4FF（電光藍）
- 輔助色：#FF6B35（暖橘，用於重要 CTA）
- 文字：#E8ECF1（主）/ #94A3B8（次）
- 卡片/區塊背景：#1E293B
- 邊框：rgba(0,212,255,0.1)

## 動畫效果
- Hero：CSS 動態網格背景 + 漸層光暈脈動
- Scroll Reveal：元素進入視窗時淡入上滑（Intersection Observer）
- 數字計數器：滾動到位時從 0 跳到目標值
- Navbar：滾動後縮小 + backdrop-filter blur
- 卡片 hover：微放大 + 邊框發光
- 服務流程：Z 字形佈局，帶連接線動畫
- 平滑滾動：scroll-behavior: smooth

## 頁面結構（單頁，以下為各 section）

### 1. Navbar（固定頂部）
- Logo：擎添工業 CHING TECH（文字 logo，CHING TECH 用強調色）
- 連結：關於我們 | 核心業務 | 技術實力 | 服務流程 | 成功案例 | 聯絡資訊
- CTA 按鈕：立即諮詢
- 手機版漢堡選單

### 2. Hero Section（全螢幕）
- 副標：自 1984 年創立 · 深耕自動化領域逾 40 年
- 主標：打造工業 4.0 **智慧工廠** 的堅實夥伴（「智慧工廠」用強調色）
- 描述：專精於機械自動控制系統、AGV/AMR無人搬運與系統整合。為您提供量身訂製的自動化解決方案，全面提升生產效能。
- 按鈕：探索解決方案（實色）+ 聯繫我們（描邊）
- 背景：動態網格 + 光暈效果
- 四角裝飾線（科技感）

### 3. 關於我們
- 左側文字：
  - 小標：ABOUT US
  - 標題：關於擎添工業 / CHING-TECH INDUSTRIAL
  - 內文：擎添工業有限公司創立於1984年，為台灣專業的工業自動化解決方案供應商。我們專精於為機械製造商及各類產業提供客製化的自動控制系統與電氣生產服務。
  - 第二段：在電腦監控系統與自動控制技術領域擁有卓越的專業能力，致力於協助客戶建構符合工業4.0標準的智慧工廠，實現企業的智慧製造轉型目標。
  - 數字區塊：40+（年產業經驗）| 1984（創立年份）| 8（大核心領域）— 計數動畫
- 右側：placeholder 圖片區塊（漸層背景 + 文字「自動化產線」）

### 4. 核心業務（8 大領域）
- 小標：OUR EXPERTISE
- 標題：核心業務領域
- 副標：提供從單機控制到整廠智慧化的一站式解決方案
- 4×2 卡片 grid，每張卡片有 Font Awesome icon + 標題 + 描述：
  1. fa-microchip — 機械自動控制系統：精密控制技術整合，為各類機械設備提供穩定的控制核心。
  2. fa-bolt — 自動電氣生產客製化：量身訂製電氣解決方案，滿足特殊製程需求。
  3. fa-desktop — 電腦監控系統：即時監控與數據管理，實現生產透明化。
  4. fa-robot — 機械手臂整合：機器人自動化應用，提升生產彈性與效率。
  5. fa-truck — 無人搬運系統：AGV/AMR智慧物流，串聯廠內物料流動。
  6. fa-chart-line — 電腦數據分析：大數據應用與優化，提供決策輔助。
  7. fa-industry — 工業4.0智慧工廠：全方位數位轉型，建置現代化智慧生產環境。
  8. fa-link — 系統整合服務：跨平台、跨品牌整合能力，確保無縫協同運作。

### 5. AGV/AMR 專區
- 左側：placeholder 圖片（漸層 + 「AGV 自動導引車」文字）
- 右側：
  - 小標：SMART LOGISTICS
  - 標題：AGV/AMR 智慧物流搬運系統
  - 描述：提供從標準型到超重載型（最高2000公斤）的自動導引車解決方案。結合高精度定位與智能調度，實現工廠物流全面自動化。
  - 三個特色（帶 check icon）：
    - 全向式移動 (AMR)：360度靈活移動，無需轉向，適應狹窄空間。
    - 智能路徑規劃：自主避障與路徑優化，效率最大化。
    - 重載能力：專為金屬加工與大型設備設計的重載方案。

### 6. 機械手臂專區
- 跟 AGV 類似但左右交換
  - 小標：ROBOTIC INTEGRATION
  - 標題：機械手臂整合應用
  - 描述：整合多品牌機械手臂（如 KUKA, FANUC, YASKAWA 等），打造高效能自動化工作站。從精密組裝到重型搬運，我們提供最適合的解決方案。
  - 三個特色：
    - 多元應用：焊接、搬運、組裝、塗膠等製程自動化。
    - 人機協作：導入協作型機器人，安全提升生產彈性。
    - 客製化程式開發：針對特殊製程需求進行邏輯開發與優化。

### 7. 服務流程（Z 字形）
- 深色背景區塊
- 小標：SERVICE PROCESS
- 標題：專業服務流程
- 副標：嚴謹的標準化作業，確保專案如期如質達成目標
- 6 步驟 Z 字形排列（上排 3 個 → 下排 3 個反向）：
  1. fa-search — 需求評估 / 現場勘查
  2. fa-drafting-compass — 方案設計 / 效益分析
  3. fa-cog — 系統建置 / 整合工程
  4. fa-check-circle — 測試驗收 / 效能調校
  5. fa-user-graduate — 教育訓練 / 操作轉移
  6. fa-headset — 售後服務 / 技術支援
- 步驟之間有水平和垂直連接線

### 8. 技術實力
- 小標：TECHNOLOGY
- 標題：堅強技術實力
- 副標：掌握自主研發關鍵技術，持續創新，從底層控制到上層管理系統，提供全方位的技術支援。
- 3 張大卡片：
  1. fa-cogs — PLC & 運動控制：精通多品牌PLC與高階運動控制算法
  2. fa-tv — SCADA & 數據可視化：工廠監控管理系統與戰情室規劃
  3. fa-network-wired — IIoT & 工業 4.0：設備聯網、數據採集與MES整合
- 技術標籤列：PLC程式設計、運動控制、SCADA系統、大數據分析、AGV/AMR技術、機器人整合

### 9. 成功案例
- 小標：CASE STUDIES
- 標題：成功案例實績
- 副標：跨足多元產業，深獲國內外知名企業信賴
- 8 個案例（4×2 grid），每個有圓形圖片 + 標題 + 描述：
  1. 半導體封測大廠 — 產線自動化與無人搬運系統（圖：https://ching-tech.com/userfiles/images/CASE/case1-1.png）
  2. 傳統金屬加工產業 — 重載型AGV (2000KG)（圖：https://ching-tech.com/userfiles/images/CASE/case10-1.jpg）
  3. 美商科技產業 — 重載AGV (600KG) ASRS系統（圖：https://ching-tech.com/userfiles/images/CASE/case11-1.jpg）
  4. 日商機械手臂產業 — 台灣安川智慧產線（圖：https://ching-tech.com/userfiles/images/CASE/case8-1.jpg）
  5. 台灣CNC加工產業 — 精密加工自動化（圖：https://ching-tech.com/userfiles/images/CASE/case7-1.jpg）
  6. 日本光學科技廠 — 烤箱料架AGV倉儲系統（圖：https://ching-tech.com/userfiles/images/CASE/case6-2.jpg）
  7. 面板廠 — 自動化物料搬運（圖：https://ching-tech.com/userfiles/images/CASE/case4-1.jpg）
  8. PCB板廠 — 重型烤箱自動化（圖：https://ching-tech.com/userfiles/images/CASE/case3-1.jpg）

### 10. 聯絡資訊
- 左側：
  - 小標：CONTACT US
  - 標題：聯絡我們
  - 描述：有任何自動化需求或專案諮詢？歡迎隨時聯繫我們，擎添專業團隊將竭誠為您服務。
  - 聯絡項目（帶 icon）：
    - fa-map-marker-alt — 公司地址：新北市五股區成泰路一段194-8號 J棟 (郵遞區號:248)
    - fa-phone — 服務專線：(02) 2903-2788
    - fa-fax — 傳真號碼：(02) 2903-9518
    - fa-globe — 官方網站：https://ching-tech.com/
  - Google 地圖連結按鈕
- 右側：placeholder 地圖區塊（漸層背景）

### 11. Footer
- 左：擎添工業 / 您值得信賴的工業自動化夥伴
- 右：© 2026 Ching-Tech Industrial Co., Ltd. All rights reserved.

## 檔案結構
```
index.html      — 唯一頁面
css/style.css   — 所有樣式
js/main.js      — 所有互動
```

刪除 about.html, solutions.html, contact.html（不再需要）。

## 品質要求
- CSS 要有層次感：卡片要有 hover 動畫、邊框發光效果
- 區塊之間要有足夠的 padding 和視覺區隔
- 手機版要完整可用（漢堡選單、單欄排列）
- 圖片 placeholder 要好看（用漸層 + icon，不是純灰色方塊）
- 服務流程的 Z 字形要在手機版變成直線
- Lighthouse Performance 目標 ≥ 90

## 注意
- 不要用 emoji 當 icon，全部用 Font Awesome
- 案例圖片從 ching-tech.com 直接引用（已有的 URL）
- 所有文案直接用上面提供的，不要自己發明
