# App Store Connect 提交指南
**Doctor Assistance 加密文件提交步驟**

## 📋 提交前檢查清單

### ✅ 必要文件準備
- [x] `Info.plist` 加密聲明設定
- [x] 加密技術規格文件
- [x] 自我分類報告
- [ ] 開發者證書和簽名設定
- [ ] App Store Connect 帳號準備

### ✅ 技術準備
- [ ] 應用程式 Build 完成
- [ ] 所有功能測試通過
- [ ] 加密功能驗證完成
- [ ] 隱私政策更新完成

## 🚀 App Store Connect 提交步驟

### 第一步：上傳 Build
1. 使用 Xcode 或 Application Loader 上傳 `.ipa` 檔案
2. 確保 `Info.plist` 包含 `ITSAppUsesNonExemptEncryption = true`

### 第二步：App Store Connect 設定

#### 2.1 應用程式資訊
- **App 名稱**: Doctor Assistance
- **副標題**: 醫護人員智能工作助理
- **分類**: 醫療 (Medical)
- **內容分級**: 4+ (無限制內容)

#### 2.2 隱私設定
在 "App 隱私" 部分：
- **收集資料類型**: 
  - ✅ 聯絡資訊 (電子郵件，用於帳號)
  - ✅ 健康與健身 (患者識別資訊)
  - ✅ 使用資料 (應用程式功能使用)
- **資料使用目的**:
  - ✅ App 功能
  - ✅ 分析
  - ❌ 第三方廣告
  - ❌ 開發者廣告

#### 2.3 年齡分級
- **年齡分級**: 4+
- **醫療/治療資訊**: 無頻繁/強烈內容

### 第三步：加密問卷回答

#### 3.1 主要問題回答
**Q: "Does your app use encryption?"**
✅ **回答: Yes**

**Q: "Does your app qualify for any of the exemptions provided in Category 5, Part 2 of the U.S. Export Administration Regulations?"**
✅ **回答: Yes**

**Q: "Does your app use encryption that's exempt under Category 5, Part 2 of the U.S. Export Administration Regulations?"**
✅ **回答: Yes - Item (b)(1) Mass Market exemption**

#### 3.2 詳細說明
在說明欄位填寫：
```
This app uses standard AES-256-GCM encryption to protect patient medical 
identification data (names, medical record numbers, admission numbers) 
stored locally on the device. The encryption is implemented using standard 
cryptographic libraries and qualifies for the Mass Market exemption under 
EAR 740.17(b)(1). The app does not include any proprietary encryption 
algorithms or cryptographic functionality beyond standard data protection.
```

### 第四步：文件上傳

#### 4.1 必要文件
在 "其他文件" 或 "法規文件" 部分上傳：

1. **`encryption-technical-specification.pdf`**
   - 標題: "Encryption Technical Specification"
   - 描述: "詳細的加密技術規格和實現說明"

2. **`self-classification-report.pdf`**
   - 標題: "Export Control Self-Classification"  
   - 描述: "出口管制自我分類報告"

#### 4.2 文件格式要求
- 格式: PDF
- 大小: < 10MB
- 語言: 英文 (必要時提供中文對照)

### 第五步：其他必要資訊

#### 5.1 應用程式說明
**簡短描述** (170 字元以內):
```
專為醫護人員設計的智能工作助理，提供安全的患者資料管理和AI語音轉文字功能。
```

**詳細描述**:
```
Doctor Assistance 是專為醫護人員設計的智能工作助理，採用醫療級 AES-256-GCM 
加密技術保護患者敏感資訊。

主要功能：
• 安全患者資料管理
• AI 語音轉文字任務建立
• HIS 系統整合 (台中榮總)
• 跨設備雲端同步
• 醫療級端到端加密

安全特色：
• AES-256-GCM 軍用級加密
• Firebase Auth 身份驗證
• 本地 iOS Keychain 安全存儲
• 零第三方追蹤和廣告

本應用程式為個人生產力工具，非醫療設備，不提供醫療診斷建議。
```

#### 5.2 關鍵字
```
醫護, 醫師, 護理師, 病人管理, 任務管理, 語音識別, 醫院, HIS, 加密, 安全
```

#### 5.3 應用程式預覽
- 準備 6.5" iPhone 螢幕截圖 (必要)
- 準備 12.9" iPad Pro 螢幕截圖 (推薦)
- 應用程式預覽影片 (可選，但推薦)

## ⚠️ 常見問題和注意事項

### Q1: 如果審核被拒怎麼辦？
**A**: 
1. 檢查拒絕原因
2. 如果是加密相關，提供更詳細的技術文件
3. 強調 Mass Market 豁免適用性
4. 如需要，諮詢出口管制法律專家

### Q2: 需要提供加密演算法實現代碼嗎？
**A**: 
通常不需要。提供技術規格文件即可。如 Apple 要求，可提供相關程式碼片段。

### Q3: 如何處理不同國家的法規要求？
**A**:
- 美國: 已通過 EAR Mass Market 豁免
- 歐盟: 符合 GDPR 技術要求  
- 其他地區: 遵循當地醫療資料保護法規

### Q4: 未來更新版本需要重新提交加密文件嗎？
**A**:
- 如果加密技術沒有重大變更：不需要
- 如果有新的加密功能：需要重新評估和提交
- 建議保持技術文件版本同步

## 📞 聯絡和支援

### Apple Developer Support
- 技術問題: Apple Developer Forums
- 審核問題: App Store Connect 提交回饋

### 出口管制諮詢
如對出口管制分類有疑問，建議諮詢：
- 出口管制法律專家
- 美國商務部 BIS (Bureau of Industry and Security)

---
**準備日期**: 2025年1月
**文件版本**: 1.0
**下次檢查**: App 重大更新時