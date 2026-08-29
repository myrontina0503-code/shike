# 食刻

個人飲食與體重管理網頁。資料存在使用者自己的 Google Drive（一個叫 `shike-data.json` 的檔案），純靜態網頁，沒有後端伺服器。

## 部署前必做：設定 Google OAuth Client ID

1. 到 [Google Cloud Console](https://console.cloud.google.com/) 建立專案並啟用 **Google Drive API**。
2. 到「憑證」頁面建立 **OAuth 用戶端 ID**，類型選「網頁應用程式」。
3. 在「授權的 JavaScript 來源」加入這個網站實際的網址（例如 `https://yourname.github.io`）。
4. 把產生的 Client ID 貼到 `index.html` 最上面的 `GOOGLE_CLIENT_ID` 常數。
5. 若 OAuth 同意畫面停留在「測試中」狀態，記得把自己的 Google 帳號加進「測試使用者」名單。

## 本機測試

純靜態檔案，用任何本機伺服器開都可以，例如：

```bash
python3 -m http.server 8000
```

再打開 `http://localhost:8000`。記得把 `http://localhost:8000` 也加進 Google Cloud Console 的「授權的 JavaScript 來源」。
