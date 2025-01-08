# vue-electron-template

基於 Vue 3 + Electron + Vite 的桌面應用程式開發模板

## 功能特點

- 🖥️ Electron 33+ 支援
- ⚡️ Vue 3 + Vite 開發環境
- 🔥 熱重載開發體驗
- 📦 開箱即用的打包配置

## 開發環境建議

- [VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar)
- Node.js 18+
- npm 或 yarn

## 快速開始

### 安裝依賴
```sh
npm install
# 或
yarn install
```

### 開發模式
```sh
# 一般 Vue 開發模式
npm run dev
# 或
yarn dev

# Electron 開發模式
npm run electron:dev
# 或
yarn electron:dev
```

### 打包應用程式
```sh
# 打包 Vue 應用程式
npm run build
# 或
yarn build

# 打包 Electron 應用程式
npm run electron:build
# 或
yarn electron:build
```

## 專案結構

```
├── electron/         # Electron 主程序相關檔案
├── src/              # Vue 應用程式源碼
├── public/           # 靜態資源
├── dist/             # Vue 建置輸出目錄
└── dist_electron/    # Electron 建置輸出目錄
```

## 構建輸出說明

執行 `npm run electron:build` 後，將在專案根目錄生成 `dist_electron` 資料夾，其結構如下：

```
dist_electron/
├── mac/                  # macOS 相關檔案（僅在 macOS 構建時出現）
│   └── {應用程式名稱}.app
├── win-unpacked/        # Windows 相關檔案（僅在 Windows 構建時出現）
│   └── {應用程式名稱}.exe
├── linux-unpacked/      # Linux 相關檔案（僅在 Linux 構建時出現）
│   └── {應用程式名稱}
└── {應用程式名稱}-{版本號}.{格式}  # 打包後的安裝檔
    # 例如：
    # - Windows: your-app-0.0.0.exe
    # - macOS: your-app-0.0.0.dmg
    # - Linux: your-app-0.0.0.AppImage
```

### 輸出檔案說明

- **Windows**: 
  - 生成 `.exe` 安裝檔
  - 支援自定義安裝目錄
  - 包含解除安裝程式

- **macOS**:
  - 生成 `.dmg` 映像檔
  - 支援拖放安裝

- **Linux**:
  - 生成 `.AppImage` 可執行檔
  - 免安裝，直接執行

> 注意：實際生成的檔案取決於您的作業系統和 `package.json` 中的 `build` 配置。

## 自定義配置

- Vite 配置：參考 [Vite 配置指南](https://vitejs.dev/config/)
- Electron 配置：修改 `electron/main.js`

## 注意事項

- 開發時請確保 Node.js 版本 >= 18
- 目前使用 Electron 33+，如需降版請注意相容性問題
- 如遇到打包問題，請檢查相關依賴版本是否兼容

## 授權

MIT License
