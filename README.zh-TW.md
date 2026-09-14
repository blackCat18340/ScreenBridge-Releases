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

最多可建立四個獨立的 Windows 顯示器，並將每個顯示器分別指派給不同的 Android
裝置。每個顯示器都能個別設定解析度、更新率、編碼格式、碼率、傳輸方式、方向與觸控。

- 使用裝置原生解析度，並支援橫向與直向顯示模式
- 提供 <code>50</code>、<code>60</code>、<code>90</code>、<code>120</code>、
  <code>144</code> 與 <code>165 FPS</code>，上限依接收端原生更新率決定
- 使用 DXGI Desktop Duplication 與 D3D11 處理畫面，支援 H.264 或 HEVC 硬體編碼
- Android MediaCodec 硬體解碼與等比例畫面輸出
- 直接觸控操作，並在 Windows 顯示游標回饋
- 每個顯示器可獨立使用 USB 或區域 Wi-Fi

已實機測試的 GPU 包括 NVIDIA GeForce RTX 3070 Ti、NVIDIA GeForce RTX 5080
與 Intel Iris Xe Graphics。實際可達解析度與更新率仍會受到硬體編碼器、Android
裝置解碼能力、電源模式及連線品質影響。

**虛擬顯示器示範**

https://github.com/user-attachments/assets/a8c16f68-1d61-40cc-97c3-aa55971791f8

### 觸控板

不建立虛擬顯示器，直接將 Android 觸控螢幕作為 Windows 觸控板。

- 游標加速、輕觸點擊、輕觸拖曳與選用的三指拖曳
- 高解析度雙指捲動、縮放與震動回饋
- 瀏覽器上一頁與下一頁手勢
- Windows 三指與四指手勢
- 手掌排除、實體尺寸校正與自適應游標濾波
- 透過虛擬 HID 操作已提權視窗與安全確認畫面

### 媒體面板

將一台或多台 USB 連接的 Android 裝置作為機殼內、桌面或其他固定位置的媒體面板。
媒體面板不會建立 Windows 顯示器，也不會啟動桌面影像編碼器。

- 多個獨立媒體面板與持久化裝置指派
- 集中管理圖片、動畫與影片素材
- 多圖層版面，支援位置、尺寸、旋轉、透明度、裁切與適應方式
- 開機自動啟動與 USB 重新連線
- 每個面板使用獨立內容與版面

**媒體面板示範**

https://github.com/user-attachments/assets/e3a7b35f-6b84-472d-9483-05761e4b38f4

### 連線與 Android 接收端管理

- USB 直接傳輸與低延遲區域 Wi-Fi 傳輸
- 初次連線使用六位數配對碼，Windows 與 Android 可分別選擇是否記住裝置
- Wi-Fi 控制與影像流量皆經過驗證與加密
- 透過 USB 偵測接收端，並由使用者確認安裝
- 沒有 USB 線時，可掃描區域網路 QR Code 下載 Android 接收端
- 透過 Wi-Fi 偵測接收端版本，並在已驗證的連線內更新 APK
- 保留顯示器、觸控板、媒體面板與裝置指派

### 效能與診斷

- 事件驅動畫面擷取與有界共用 GPU texture pool，避免重複編碼靜止畫面及累積過時影格
- Wi-Fi 影像封包節奏控制、短期封包重排與自適應 Reed-Solomon 遺失修復
- 分別顯示傳輸、MediaCodec 解碼與 Android 畫面呈現延遲
- Windows 設定中的結構化診斷日誌，可依層級、元件、工作階段、傳輸方式、時間與文字篩選

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
