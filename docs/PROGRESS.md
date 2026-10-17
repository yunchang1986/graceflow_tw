# GraceFlow Landing Page 進度

## 2026-08-19 v1 初版

### 決策
- **定位**：Amber Chang 個人品牌頁，AI Project Lead / TPM（正式職稱：逢甲大學 AI 研究中心執行副主任）
- **語言**：中英雙語，預設中文，右上角切換（localStorage 記住偏好）
- **內容隱私**：只放領域經驗，不放客戶名稱與專案數據（RTP 等客戶敏感資訊不上公開網頁）
- **部署**：GitHub Pages + 自訂網域 graceflow.tw（CNAME 檔已建）
- **聯絡方式**：Email + LinkedIn + LINE 官方帳號（電話不公開）
- **設計**：暖石灰近單色 + 琥珀色點綴（呼應 Amber）、Archivo + Noto Sans TC、支援深色模式與 prefers-reduced-motion

## 2026-08-19 推上 GitHub

- Repo：`yunchang1986/graceflow_tw`（私有），本地工作目錄 `~/github/graceflow_tw`（以此為準，`~/graceflow.tw` 為初版草稿可刪）
- ⚠️ 私有 repo 開 GitHub Pages 需要 GitHub Pro；若不升級，改用 Cloudflare Pages 連私有 repo 部署

## 2026-08-20 正式上線 + v2 改版

- Repo 改為公開，GitHub Pages 啟用（main / root），自訂網域 graceflow.tw
- Cloudflare DNS 已切換（API 完成）：根網域四筆 A → GitHub Pages IP、www CNAME → yunchang1986.github.io，皆 DNS only；郵件記錄（Google MX、Gandi SRV/TXT）未動
- HTTPS 憑證已簽發，Enforce HTTPS 已開啟（http → https 301）
- **v2 改版**：採用 3B「Light Cross Flow」標誌（無限流動曲線 + 中心光十字）+ Concept 4 薰衣草紫色系；字體改 Cormorant Garamond + Noto Serif TC（標題）
- 網站：https://graceflow.tw

### 待辦
- [ ] LinkedIn 個人檔案網址（index.html 內 TODO，目前是 linkedin.com 首頁）
- [ ] 建立 LINE 官方帳號後，換上 lin.ee 加入好友連結並移除按鈕的 `hidden`
- [ ] 學歷「靜宜碩士 vs 學士」層級待確認（見 ~/Downloads/Amber_Chang_正式資料_official_20260819.txt）

### 相關檔案
- 正式個人資料：`~/Downloads/Amber_Chang_正式資料_official_20260819.txt`
- 履歷素材彙整：`~/Downloads/amber-cv-source-consolidated-20260819.md`

## 2026-10-18 Brand Kit 總覽板

- 產出 3×3 品牌識別總覽板：`docs/brand/graceflow-brandkit.png`（3200×2400），原始檔 `docs/brand/brandkit.html`
- 作法：AI 生圖兩條路都失敗（Gemini 免費額度用盡、Azure gpt-image-2 回 `response_format` 參數錯誤），改用 HTML + 網站原始 SVG 標誌，以 headless Chrome 渲染；好處是標誌、色碼、字體與網站 100% 一致
- 九格：主標誌 / 標誌構成 / 網站 / 品牌核心句 / 色彩 / 字體 / 名片 / 影像方向 / 系統元件
- 重新輸出：`"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --hide-scrollbars --force-device-scale-factor=2 --window-size=1600,1200 --virtual-time-budget=8000 --screenshot=docs/brand/graceflow-brandkit.png file://$PWD/docs/brand/brandkit.html`

## 2026-10-18 UI/UX 稽核修正（index.html）

- 修：hero 在手機上左右沒有內距（`.hero` 的 padding 蓋掉 `.wrap` 的 24px 側距），文字貼齊螢幕邊緣；手機版上方留白縮為 56px
- 修：`.reveal` 淡入動畫改由 `html.js` 控制，JS 失效時內容不再整段隱形
- 修：錨點跳轉被 sticky header 遮住 → section 加 `scroll-margin-top: 64px`
- 修：標題層級 h1→h3 跳級 → 區塊標籤改為 h2（外觀不變）
- 修：語言切換按鈕高度 40→44px（觸控目標）；品牌連結補 focus-visible 外框
- 修：手機版 h1 最後一行只剩「統。」→「AI 系統。」不斷行
- 已檢查：文字對比淺色/深色模式皆 ≥ 5:1（AA 通過）
- 未做（建議）：Open Graph 分享預覽（og:title / og:image），LinkedIn 分享時目前沒有預覽圖

## 2026-10-18 Logo 重新設計：三個提案

- 提案板：`docs/brand/graceflow-logo-proposals.png`，原始檔 `docs/brand/logo-proposals.html`（SVG 手繪，與網站同色系）
- A「光心 G」：一筆開口 G + 中心金點；原本帶橫槓的版本太像 Google G，已改成短收尾
- B「匯流 Confluence」：三線匯成一線指向金點＝跨職能對齊→交付
- C「水上之光」：圓形印記，地平線上的光與倒影之路＝Light in the Path
- 待決：使用者選定方向 → 精修（字距、16px 版本）→ 換上網站與 favicon、更新 brand kit
