📊 台灣吸菸行為數據監測系統 (Taiwan Smoking Data Dashboard)

這是一個基於 ASP.NET Core MVC 後端架構與 D3.js 數據視覺化技術開發的互動式儀表板。透過此系統，使用者可以直觀地觀察台灣各縣市在不同年份及對象（成人、高中職學生、國中學生）的吸菸行為趨勢。
🌟 核心功能

    互動式地圖：使用 D3.js 渲染 TopoJSON 地圖，支援滑鼠懸浮顯示各縣市詳細數據。

    多維度篩選：支援切換「觀察對象」（成人、高中職、國中）與「統計年份」。

    即時數據指標：自動計算並顯示全台年度平均值。

    響應式佈局：地圖具備自動縮放功能（viewBox），適應各種螢幕尺寸。

    熱圖視覺化：根據數值高低自動映射顏色深淺（使用 interpolateReds）。

🛠️ 技術棧

    後端：ASP.NET Core 7.0/8.0 MVC

    前端：JavaScript (ES6+), D3.js v7, TopoJSON, CSS3, Bootstrap 5

    數據格式：JSON (包含台灣縣市地形資料與監測數據)

📂 專案結構
```Plaintest
WebApplication1/
├── Controllers/            # MVC 控制器
├── Views/
│   ├── Home/Index.cshtml   # 主要儀表板頁面
│   └── Shared/_Layout.cshtml # 全域版面設定
├── wwwroot/                # 靜態資源檔案
│   ├── css/style.css       # 自定義佈局樣式
│   ├── js/script.js        # D3.js 地圖渲染邏輯
│   └── data/               # 資料來源檔案
│       ├── data.json       # 吸菸統計數據
│       └── taiwan.json     # 台灣地形地圖資料
└── Program.cs              # .NET 程式進入點
```
🚀 快速開始
1. 複製專案
 ```
git clone https://github.com/您的帳號/TaiwanSmokingDataMap.git
```
2. 環境要求

    Visual Studio 2022 (或以上)

    .NET 7.0/8.0 SDK

3. 執行

    使用 Visual Studio 開啟 .sln 方案檔。

    確保 data.json 與 taiwan.json 位於 wwwroot/data/ 資料夾中。

    按 F5 執行專案。

📝 數據來源

數據整合自台灣政府開放資料，包含各縣市 15 歲以上成人每日吸菸支數及青少年吸菸率統計。
