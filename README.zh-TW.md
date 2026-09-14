<p align="center">
  <img
    src="assets/screenbridge-windows.png"
    alt="ScreenBridge"
    width="180">
</p>

<h1 align="center">ScreenBridge 下載</h1>

<p align="center">
  <strong>將 Android 裝置變成 Windows 顯示器、觸控板或媒體面板。</strong>
</p>

<p align="center">
  <a href="README.md">English</a> |
  <strong>繁體中文</strong>
</p>

## 下載

請從 [ScreenBridge Releases](https://github.com/blackCat18340/ScreenBridge-Releases/releases/latest)
下載最新的 <code>ScreenBridge-&lt;version&gt;-win-x64-setup.exe</code>。

自包含安裝程式內含 Windows 應用程式、ScreenBridge 虛擬顯示與輸入驅動程式、Android
接收端、USB 傳輸工具及解除安裝程式。使用者不需要另外安裝 .NET runtime。

## 功能

### 虛擬顯示器

- 最多四個獨立 Windows 虛擬顯示器
- USB 或已驗證的區域 Wi-Fi 傳輸
- Android 原生解析度、橫向與直向顯示模式
- H.264 與 HEVC 硬體編碼
- 高更新率串流與 Android 直接觸控輸入

**虛擬顯示器示範**

https://github.com/user-attachments/assets/a8c16f68-1d61-40cc-97c3-aa55971791f8

### 觸控板

- 游標移動、點擊、拖曳、捲動與縮放
- 瀏覽器上一頁與下一頁
- Windows 三指與四指手勢
- 手掌排除、震動回饋與選用的三指拖曳
- 可操作提權 Windows 畫面與安全提示的虛擬 HID 輸入

### 媒體面板

- 多個獨立 USB 媒體面板
- 集中管理圖片、動畫與影片素材
- 支援裁切與適應方式的多圖層版面編輯器
- 持久化裝置指派、自動啟動與 USB 重新連線

**媒體面板示範**

https://github.com/user-attachments/assets/e3a7b35f-6b84-472d-9483-05761e4b38f4

## 系統需求

- Windows 11 x64
- Android 11 或更新版本
- 支援 H.264 硬體編碼的 GPU；HEVC 需要 Windows 與 Android 硬體同時支援
- 已啟用 Android USB 偵錯且支援資料傳輸的 USB 連線，或位於相同區域 IPv4
  網路的兩端裝置
- 安裝驅動程式所需的系統管理員權限

使用 Wi-Fi 時，建議採用干擾較少的 5 GHz 或 6 GHz 區域連線。

> [!NOTE]
> Windows 安裝程式尚未使用 Authenticode 簽署。ScreenBridge 虛擬顯示與輸入
> 驅動程式使用開發測試憑證，隨附的 Android 接收端則使用固定的 ScreenBridge
> 發行簽章。

原始碼、建置方式與架構文件位於
[ScreenBridge 專案](https://github.com/blackCat18340/ScreenBridge)。
