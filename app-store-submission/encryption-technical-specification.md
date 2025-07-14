# Doctor Assistance - 加密技術規格文件
**App Store Connect 提交用文件**

## 應用程式資訊
- **應用程式名稱**: Doctor Assistance (DRAssistance)
- **開發者**: [您的開發者名稱]
- **Bundle ID**: com.example.drassistance
- **版本**: 1.0.0
- **類別**: 醫療應用

## 加密使用聲明

### 加密目的
本應用程式使用加密技術保護醫護人員的患者識別資訊，確保醫療數據的隱私和安全。

### 加密範圍
**僅加密以下患者敏感識別資訊：**
- 患者姓名
- 病歷號碼  
- 住院號碼

**不加密的資料：**
- 床號、年齡、性別等非敏感資訊
- 個人任務和備忘錄
- 醫師個人設定

## 技術規格詳細說明

### 1. 主要加密算法
- **算法**: AES-256-GCM (Advanced Encryption Standard with Galois/Counter Mode)
- **金鑰長度**: 256-bit (32 bytes)
- **認證**: NIST FIPS 197 認可的標準算法
- **模式**: GCM 提供認證加密 (AEAD - Authenticated Encryption with Additional Data)
- **完整性保護**: 內建防篡改驗證

### 2. 金鑰管理
- **金鑰派生**: PBKDF2 with HMAC-SHA256
- **迭代次數**: 100,000 次 (符合 NIST SP 800-132 建議)
- **鹽值長度**: 256-bit (32 bytes)
- **隨機數生成**: 使用密碼學安全隨機數生成器 (CSPRNG)

### 3. 初始向量 (IV)
- **長度**: 128-bit (16 bytes)
- **生成**: 每次加密使用新的隨機 IV
- **唯一性**: 確保相同明文產生不同密文

### 4. 實現庫
- **主要庫**: PointyCastle (Dart/Flutter 生態系統)
- **輔助庫**: 
  - `crypto` package (Flutter 官方)
  - `flutter_secure_storage` (iOS Keychain / Android Keystore)

### 5. 存儲安全
- **iOS**: 使用 Keychain Services 存儲加密金鑰
- **Android**: 使用 Android Keystore 系統
- **Web**: 使用加密的 localStorage

## 法規合規性

### Export Administration Regulations (EAR) 分析
- **分類**: 5D002.c.1 (Mass Market 軟體)
- **適用豁免**: EAR 740.17(b)(1) Mass Market 豁免
- **理由**: 
  - 使用標準商業加密算法
  - 金鑰長度在許可範圍內 (≤256-bit 對稱)
  - 非軍事/政府用途
  - 商業醫療應用

### 技術標準合規
- **NIST**: 符合 NIST SP 800-57 金鑰管理建議
- **FIPS**: 使用 FIPS 197 認可的 AES 算法
- **RFC**: 符合 RFC 5116 (AEAD) 標準

## 安全設計原則

### 1. 最小權限原則
- 僅對真正敏感的患者識別資訊進行加密
- 非敏感資料保持明文，提升性能

### 2. 防禦深度
- 本地加密 + 傳輸加密 (HTTPS)
- 用戶級別金鑰隔離
- 自動金鑰輪換機制

### 3. 透明性
- 明確告知用戶哪些資料被加密
- 提供加密狀態指示器
- 用戶可選擇性使用加密功能

## 第三方服務聲明

### Cloudflare Workers AI
- **用途**: 僅用於語音轉文字處理
- **資料處理**: 
  - 音頻資料即時處理，不存儲
  - 處理完成後立即銷毀原始音頻
  - 僅返回轉換後的文字內容
- **可選性**: 用戶可選擇不使用語音功能

### Firebase Services
- **用途**: 身份驗證和資料同步
- **配置**: 未啟用 Analytics 或其他追蹤服務
- **資料**: 僅存儲加密後的患者識別資訊

## 結論

本應用程式使用標準的商業加密技術保護醫療數據，符合 Mass Market 軟體的定義，適用於 EAR 740.17(b)(1) 豁免條款。所有加密實現均基於國際認可的標準算法，不涉及專有或軍用加密技術。

---
**文件準備日期**: 2025年1月
**聯絡資訊**: [您的聯絡方式]
**技術負責人**: [技術負責人資訊]