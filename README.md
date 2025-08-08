# Excel數據處理積木化應用本地版 (Block-based Excel Data Processing Application)

這是一個本地運行的桌面應用程式，旨在通過拖拽積木的方式，讓用戶能夠直觀地建立Excel數據處理流程。本項目專為個人用戶設計，無需網路連接即可完整運行。

## 核心特色

- **完全本地化**：無需網路連接，數據完全保留在本地電腦，確保隱私和安全。
- **輕量高效**：專為個人使用優化，啟動快速、資源佔用低。
- **簡單易用**：提供直觀的拖拽界面，讓不具備編程背景的用戶也能快速建立數據處理流程。
- **多格式輸出**：支援將處理流程導出為腳本，或打包成獨立應用程式。

## 技術棧

本項目採用以下技術構建：

- **桌面應用框架**: [Electron](https://www.electronjs.org/)
- **前端界面**: [React](https://reactjs.org/) + [TypeScript](https://www.typescriptlang.org/)
- **UI組件庫**: [Ant Design](https://ant.design/)
- **構建工具**: [Vite](https://vitejs.dev/)
- **狀態管理**: [Zustand](https://github.com/pmndrs/zustand)
- **核心文件處理**: [SheetJS](https://sheetjs.com/), [Papa Parse](https://www.papaparse.com/)

## 項目結構

```
/
├── /projects/              # 用戶項目文件 (*.json)
├── /config/                # 用戶設定 (settings.json)
├── /templates/             # 流程範本
├── /blocks/                # 積木定義 (*.json)
├── /src/                   # 前端React源代碼
│   ├── index.html          # HTML入口
│   └── main.jsx            # React應用主文件
├── main.js                 # Electron主程序入口
├── preload.js              # Electron預加載腳本
├── package.json            # Node.js項目配置
└── vite.config.js          # Vite配置
```

## 如何開始

### 開發模式

1.  **安裝依賴**:
    ```bash
    npm install
    ```
2.  **啟動Vite開發服務器**:
    在一個終端中運行：
    ```bash
    npm run dev
    ```
3.  **啟動Electron應用**:
    在另一個終端中運行：
    ```bash
    npm start
    ```
    應用程式將會啟動，並加載由Vite服務的React前端界面。

### 構建應用

運行以下命令來使用Vite構建前端資源：
```bash
npm run build
```
構建後的資源將會輸出到 `dist` 文件夾中。生產模式下的Electron應用將會從此文件夾加載界面。
