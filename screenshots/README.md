# 截圖使用說明

## 📸 截圖列表

將以下截圖放入此目錄，網頁會自動顯示：

### 首頁 (index.html) - 英雄區
- `app-main-screen.png` - 應用程式主畫面截圖 (建議尺寸: 375x812px)

### 首頁 (index.html) - 多設備展示區
- `patient-list.png` - 病人列表畫面 (建議尺寸: 375x812px)
- `task-detail.png` - 任務詳情畫面 (建議尺寸: 375x812px)
- `voice-input.png` - 語音輸入畫面 (建議尺寸: 375x812px)
- `security-screen.png` - 安全設定畫面 (建議尺寸: 375x812px)

### 功能頁面 (features.html)
- `task-management.png` - 任務管理功能截圖 (建議尺寸: 800x600px)
- `voice-to-task.png` - 語音轉任務功能截圖 (建議尺寸: 800x600px)

### 安全頁面 (security.html)
- `encryption-settings.png` - 加密設定界面截圖 (建議尺寸: 400x600px)

## 🔧 啟用截圖顯示

截圖就緒後，需要修改對應 HTML 檔案：

1. 將截圖的 `style="display: none;"` 改為 `style="display: block;"`
2. 將對應佔位符的 `display: flex;` 改為 `display: none;`

### 範例修改：

```html
<!-- 修改前 -->
<img src="screenshots/app-main-screen.png" alt="主畫面截圖" style="display: none;">
<div class="screenshot-placeholder" style="display: flex;">佔位符</div>

<!-- 修改後 -->
<img src="screenshots/app-main-screen.png" alt="主畫面截圖" style="display: block;">
<div class="screenshot-placeholder" style="display: none;">佔位符</div>
```

## 📱 截圖建議

- **解析度**: 使用高解析度截圖確保清晰度
- **內容**: 選擇具代表性的畫面，展示核心功能
- **格式**: 建議使用 PNG 格式保持品質
- **大小**: 壓縮檔案大小以加快網頁載入速度

## 🎯 截圖重點

1. **主畫面截圖**: 展示病人列表、任務概覽
2. **任務管理截圖**: 展示任務建立、分類、完成狀態
3. **語音功能截圖**: 展示語音輸入界面、AI轉換結果
4. **加密設定截圖**: 展示設定頁面、安全功能