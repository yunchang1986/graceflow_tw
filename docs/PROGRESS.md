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
