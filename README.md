# 瀏覽器桌面提醒鬧鐘 (進階版)

一個簡潔的瀏覽器端鬧鐘提醒應用程式，使用 React + Tailwind CSS 建構，支援桌面通知功能。

## 功能特色

- 🔔 **桌面通知**：透過瀏覽器 Notification API 發送提醒
- ⏰ **單次提醒**：設定開始時間與結束時間，支援時間範圍提醒
- 🔄 **每週重複**：可選擇特定星期幾重複執行
- ⏱️ **多階段通知**：提前 3 分鐘、1 分鐘、到點共 3 次通知
- 💾 **本地儲存**：資料儲存於 localStorage，關閉瀏覽器後仍保留

## 快速開始

### 方法一：直接開啟 (有限制)
直接用瀏覽器開啟 `index.html`，但 `file://` 協定可能導致通知功能受限。

### 方法二：使用本地伺服器 (建議)

```bash
# 使用 Node.js http-server
npx http-server -p 8080

# 或使用 Python
python -m http.server 8080
```

然後開啟瀏覽器訪問：http://127.0.0.1:8080

## 使用說明

1. 首次使用請點擊「啟用通知」按鈕授權桌面通知
2. 選擇「單次提醒」或「每週重複」模式
3. 填寫提醒事項名稱
4. 設定開始時間（與選填的結束時間）
5. 點擊「加入」按鈕完成新增

## 技術架構

- **前端框架**：React 18 (CDN)
- **樣式**：Tailwind CSS (CDN)
- **通知**：Browser Notification API
- **儲存**：localStorage

## 專案結構

```
├── index.html                      # 主程式（含 React 元件）
├── alarm.html                      # 備份檔案
├── .gitignore                      # Git 忽略規則
├── README.md                       # 本文件
└── .github/workflows/deploy.yml    # GitHub Actions 自動部署
```

## 部署到 GitHub Pages

本專案已設定 GitHub Actions 自動部署，推送到 `main` 分支即自動更新。

### 首次部署步驟

1. 在 GitHub 建立新的 Repository

2. 推送程式碼：
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/你的帳號/你的repo名稱.git
git push -u origin main
```

3. 啟用 GitHub Pages：
   - 進入 Repository → Settings → Pages
   - Source 選擇 **GitHub Actions**
   - 等待 Actions 執行完成

4. 訪問網站：`https://你的帳號.github.io/你的repo名稱/`

## 瀏覽器支援

- Chrome / Edge (建議)
- Firefox
- Safari

> ⚠️ 請確保瀏覽器已允許網站發送通知

## License

MIT
