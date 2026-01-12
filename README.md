# 南寮漁港 App - Deep Link 設定

簡單的 GitHub Pages Deep Link 配置，支援 Android App Links 和 iOS Universal Links。

## 🚀 使用方式

1. **修改配置檔案中的佔位符**
2. **部署到 GitHub Pages**
3. **測試 QR Code**：`https://<username>.github.io/<repo>/intro.html?spot=2402`

## 📝 需要修改的佔位符

- `.well-known/assetlinks.json`：
  - `<你的.package.name>` → Android package name
  - `<你的 SHA256>` → Android keystore SHA256 指紋

- `.well-known/apple-app-site-association`：
  - `<你的 TEAMID>` → Apple Team ID  
  - `<你的.bundle.id>` → iOS Bundle ID

- `intro.html`：
  - `<username>` → GitHub 用戶名
  - `<repo>` → repository 名稱

## 💡 運作原理

- **已安裝 App**：自動開啟 App 並導向指定頁面
- **未安裝 App**：顯示下載導引頁面

## ⚠️ 注意事項

- Android App Links 驗證需 15分鐘-24小時生效
- iOS Universal Links 驗證需幾分鐘-幾小時生效  
- 修改 App 配置後需重新安裝 App