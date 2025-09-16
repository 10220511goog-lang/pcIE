# Basilisk Taiwan 網站部署指南

## 專案概述
- **專案名稱**: Basilisk Taiwan 企業網站
- **技術棧**: React + Vite + Tailwind CSS + shadcn/ui
- **專案路徑**: `/home/ubuntu/basilisk-website`
- **建置輸出**: `/home/ubuntu/basilisk-website/dist`

## 部署到 Netlify 的步驟

### 1. 準備 GitHub 儲存庫
```bash
# 在專案目錄中初始化 Git（如果尚未初始化）
cd /home/ubuntu/basilisk-website
git init
git add .
git commit -m "Initial commit: Basilisk Taiwan website"

# 連接到您的 GitHub 儲存庫
git remote add origin https://github.com/YOUR_USERNAME/basilisk-website.git
git branch -M main
git push -u origin main
```

### 2. Netlify 部署設定
1. 登入 [Netlify](https://netlify.com)
2. 點擊 "New site from Git"
3. 選擇 GitHub 並授權
4. 選擇您的 `basilisk-website` 儲存庫
5. 設定建置參數：
   - **Build command**: `pnpm run build`
   - **Publish directory**: `dist`
   - **Node version**: `18` (在環境變數中設定 `NODE_VERSION=18`)

### 3. 環境變數設定（如需要）
在 Netlify 的 Site settings > Environment variables 中設定：
- `NODE_VERSION`: `18`
- 其他必要的環境變數

### 4. 自定義域名設定（可選）
1. 在 Netlify 的 Domain settings 中
2. 添加自定義域名
3. 設定 DNS 記錄指向 Netlify

## 本地建置驗證

### 建置命令
```bash
cd /home/ubuntu/basilisk-website
pnpm run build
```

### 預覽建置結果
```bash
pnpm run preview
```

## 專案結構
```
basilisk-website/
├── public/                 # 靜態資源
├── src/
│   ├── assets/            # 圖片素材
│   ├── components/        # React 組件
│   │   ├── ui/           # shadcn/ui 組件
│   │   ├── Home.jsx      # 首頁
│   │   ├── Technology.jsx # 產品原理
│   │   ├── Products.jsx  # 產品頁面
│   │   ├── Projects.jsx  # 工程實績
│   │   ├── Videos.jsx    # 影片專區
│   │   ├── FAQ.jsx       # 常見問題
│   │   ├── About.jsx     # 關於我們
│   │   ├── Contact.jsx   # 聯絡我們
│   │   ├── Navbar.jsx    # 導航欄
│   │   └── Footer.jsx    # 頁腳
│   ├── App.jsx           # 主應用組件
│   ├── App.css           # 樣式文件
│   └── main.jsx          # 入口文件
├── dist/                  # 建置輸出目錄
├── package.json
└── vite.config.js
```

## 功能特色
- ✅ 響應式設計，支援桌面和行動裝置
- ✅ 現代化 UI 設計，使用 shadcn/ui 組件
- ✅ 完整的企業網站功能
- ✅ SEO 友善的結構
- ✅ 快速載入和優化的效能

## 維護和更新
1. 修改程式碼後提交到 GitHub
2. Netlify 會自動觸發重新部署
3. 檢查部署狀態和網站功能

## 聯絡資訊
如有技術問題，請參考：
- React 官方文檔: https://react.dev
- Vite 官方文檔: https://vitejs.dev
- Tailwind CSS: https://tailwindcss.com
- shadcn/ui: https://ui.shadcn.com

