# 悅聲專業音響 網站模板

## 檔案
- `index.html`：網站首頁（關於、服務、建案實績、產品、線上估價、聯絡、線上小幫手）
- `admin.html`：內容管理後台（新增／修改建案、產品、自動回覆、估價單價、公司資訊）
- `assets/data.js`：所有網站內容。後台匯出的新檔取代它就能更新網站。
- `assets/logo.png`、`assets/hero.jpg`、`assets/projects/`、`assets/products/`、`assets/gallery/`：LOGO、建案、產品與施工實景照片

## 怎麼更新內容
1. 打開 `admin.html` 編輯，按「儲存草稿並預覽」，回到網站確認。
2. 到「匯出發布」下載 `data.js`，取代 `assets/data.js` 後上傳到主機。
3. 新照片建議放進 `assets/projects/`，在後台填檔名（直接上傳也可以，但會讓 data.js 變大）。

## 目前是展示版的部分（正式上線需要後端）
- **估價表單、聯絡表單**：現在只在畫面上顯示收到，沒有寄出。可接 Google 表單／Apps Script、Formspree 或自建後端寄到公司信箱。
- **線上小幫手**：關鍵字規則回覆。若要真人接手或 AI 回覆，可串接 LINE 官方帳號、或 AI 客服服務（需要後端與 API 金鑰）。
- **後台**：沒有登入保護，草稿只存在當下這台電腦的瀏覽器。正式版建議改用有帳號登入的 CMS（例如 Decap CMS + Netlify、或 WordPress）。

## 本機預覽
解壓縮後直接雙擊 `index.html` 就能用瀏覽器打開（後台是 `admin.html`）。

## 讓 Google 搜尋得到（SEO）
網站已內建：搜尋結果標題與描述（含「音響工程」等關鍵字）、公司資料標記（LocalBusiness 結構化資料）、`robots.txt`、`sitemap.xml`，後台設為不被搜尋。

上線時要做：
1. 把 `index.html`、`robots.txt`、`sitemap.xml` 裡所有 `https://www.example.com.tw` 換成正式網址。
2. **Google 商家檔案**（business.google.com，免費）：用公司地址申請，Google 會寄明信片或用影片驗證。這是在 Google 地圖和「音響工程 桃園」這類在地搜尋出現的最重要一步。
3. **Google Search Console**（search.google.com/search-console，免費）：驗證網域後提交 `sitemap.xml`，就能看到被搜尋的關鍵字與排名。
4. （選用）Bing Webmaster Tools：可直接從 Search Console 匯入。
5. 持續新增建案實績與施工照片，並請客戶在 Google 商家留評論，對排名幫助最大。
