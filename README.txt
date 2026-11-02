沖繩四天三夜 PWA 安裝包
==========================

檔案內容
- index.html：旅遊網站本體
- manifest.webmanifest：手機安裝資訊
- service-worker.js：網站離線快取
- icons/：桌面圖示

重要：PWA 必須部署在 HTTPS 網址（或 localhost）才能安裝與使用離線快取。
單純把 ZIP 或 HTML 存在手機，不會自動成為可安裝的 PWA。

建議部署方式（GitHub Pages）
1. 在 GitHub 建立一個新的 Public repository。
2. 將 ZIP 解壓縮，將 index.html、manifest.webmanifest、service-worker.js 和 icons 資料夾全部上傳到 repository 根目錄。
3. 進入 Settings → Pages。
4. 在 Build and deployment 選擇 Deploy from a branch。
5. Branch 選 main，資料夾選 /(root)，按 Save。
6. 等待 GitHub Pages 提供 https://... 網址。
7. 用 Android 手機 Chrome 開啟該 HTTPS 網址。
8. 點選頁面出現的「安裝」提示，或 Chrome ⋮ →「安裝應用程式／新增至主畫面」。

更新網站時，重新上傳檔案並提高 service-worker.js 的 CACHE_NAME 版本，例如 v2。
第一次開啟時請保持網路連線，讓網站完成快取；之後已快取的網站本體可離線開啟。
天氣查詢仍需要網路。
