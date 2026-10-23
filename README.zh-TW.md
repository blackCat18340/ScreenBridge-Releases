<p align="center">
  <img src="assets/screenbridge-windows.png" alt="ScreenBridge" width="160">
</p>

<h1 align="center">ScreenBridge</h1>

<p align="center">
  <strong>將 Android 裝置變成 Windows 的延伸螢幕、觸控板、媒體面板或控制台。</strong>
</p>

<p align="center">
  <a href="README.md">English</a> | <strong>繁體中文</strong>
</p>

<p align="center">
  <a href="https://github.com/blackCat18340/ScreenBridge-Releases/releases/download/v0.8.1/ScreenBridge-0.8.1-win-x64-setup.exe">下載 Windows 版 · 0.8.1</a>
</p>

讓 Android 手機或平板在桌上多一種用途。ScreenBridge 可延伸 Windows 桌面、
透過觸控操作游標、展示媒體與硬體資訊，或建立日常應用程式的控制台。
控制台也能直接在 Windows 桌面使用。

目前版本：**0.8.1**。[更新內容](https://github.com/blackCat18340/ScreenBridge-Releases/releases/tag/v0.8.1)
· [所有版本](https://github.com/blackCat18340/ScreenBridge-Releases/releases)

## 功能

### 延伸螢幕

最多可建立四個獨立的 Windows 顯示器，分別指派給不同 Android 裝置。
每個螢幕可個別設定解析度、方向、更新率與畫質，透過 USB 或區域 Wi-Fi 連線，
並直接使用觸控螢幕操作 Windows。

- 支援裝置原生解析度、橫向與直向顯示
- 提供 50、60、90、120、144 與 165 FPS，上限依裝置更新率決定
- 在支援的硬體上使用 H.264 或 HEVC

**虛擬顯示器示範**

https://github.com/user-attachments/assets/d35894fd-10f0-4a94-9480-b9b4f3ed1321

### 觸控板

將 Android 觸控螢幕作為 Windows 觸控板，支援輕觸點擊、拖曳、雙指捲動與縮放、
瀏覽器導覽，以及三指與四指手勢。游標控制也能用於已提權的 Windows 畫面。

### 媒體面板

把透過 USB 連接的 Android 裝置放在桌面或機殼內，使用多圖層版面組合圖片、動畫
與影片，加入 CPU、GPU、記憶體、儲存裝置及網路資訊。可儲存多個面板，
各自保留內容，並在裝置重新連接後自動啟動。

**媒體面板示範**

https://github.com/user-attachments/assets/100bfb60-0fad-40a2-a161-0e92730b7cb8

### 控制台

把快捷操作、音樂、音效、燈光與硬體資訊放在手邊。自訂按鍵、分頁、圖示與標籤，
並在切換 Windows 應用程式時自動換用對應版面。

- 啟動程式、輸入文字、執行快捷鍵，以及控制 OBS 場景與錄影。
- 瀏覽 Spotify 歌曲、控制播放並調整音量。
- 透過原本的麥克風，將音效與人聲一起送出。
- 控制智慧燈光的開關、亮度、色溫與顏色。
- 同一按鍵可分別設定短按、連按兩下與長按動作。
- 使用 `.sbdeck` 檔案備份與分享版面。

Android 控制台可透過 USB 或加密 Wi-Fi 連線；也能按 `Ctrl+Shift+Space`，
在游標位置叫出置頂的桌面控制台。桌面 Key Size 可調整桌面控制台尺寸，
不影響手機版面。

**虛擬控制台示範**

https://github.com/user-attachments/assets/66043f70-a838-4114-9e4b-23f26a99b960

## 安裝與開始使用

1. 下載並執行 [ScreenBridge-0.8.1-win-x64-setup.exe](https://github.com/blackCat18340/ScreenBridge-Releases/releases/download/v0.8.1/ScreenBridge-0.8.1-win-x64-setup.exe)。
2. 使用已啟用 USB 偵錯的 Android 裝置連接電腦，或讓 Windows 與 Android 位於同一
   區域網路。ScreenBridge 可透過 USB 安裝接收端；沒有傳輸線時，開啟
   **設定 > Android 應用程式 > 取得應用程式** 並掃描 QR Code。
3. 保持 Android 接收端開啟。在 ScreenBridge 選擇 `+`，新增「顯示器」、「觸控板」、
   「媒體面板」或「虛擬控制台」。
4. 選擇裝置與設定後啟動；初次連線時，在兩端確認相同的配對碼。

安裝程式內含 Windows 應用程式、顯示與輸入驅動程式、麥克風音訊元件、Android
接收端及 USB 工具，不需要另外安裝 .NET runtime。

### 在語音軟體使用音效

在控制台設定選擇實體麥克風，語音軟體也繼續選用同一支麥克風，再將音效加入控制台
按鍵。每個音效動作可設定 0～200% 音量，控制台設定另有此電腦共用的 0～100%
音效總音量。本機播放跟隨 Windows 預設輸出。

### 連接 Spotify

使用 Spotify Premium 帳號，在 [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/create)
註冊應用程式，將 Redirect URI 設為 `http://127.0.0.1:28187/spotify/`，
再將 Client ID 填入 ScreenBridge 的「連接 Spotify」對話框，完成帳號授權。

## 系統需求

- Windows 11 x64
- 手機與平板模式需要 Android 11 或更新版本
- 安裝時需要系統管理員權限
- 支援資料傳輸且已啟用 USB 偵錯的 USB 連線，或位於相同區域 IPv4 網路的兩端裝置
- 延伸螢幕模式需要支援 H.264 硬體編碼的 GPU；HEVC 另需 Android 支援解碼

Wi-Fi 串流建議使用干擾較少的 5 GHz 或 6 GHz 區域連線。媒體面板使用 USB。

> [!NOTE]
> Windows 安裝程式尚未使用 Authenticode 簽署。顯示與輸入驅動程式使用開發測試憑證，
> Android 接收端使用 ScreenBridge 發行簽章。

安裝檔雜湊收據與套件檔案清單位於
[v0.8.1 發布附件](https://github.com/blackCat18340/ScreenBridge-Releases/releases/tag/v0.8.1)。
