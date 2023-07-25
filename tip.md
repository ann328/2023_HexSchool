## 指令列表

- `npm install` - 初次下載該範例專案後，需要使用 npm install 來安裝套件
- `npm run dev` - 執行開發模式
  - 若沒有自動開啟瀏覽器，可嘗試手動在瀏覽器上輸入
    `http://localhost:5173/<專案名稱>/pages/index.html`
- `npm run build` - 執行編譯模式（不會開啟瀏覽器）
- `npm ru deploy` - 自動化部署

## 資料夾結構

- assets # 靜態資源放置處

  - images # 圖片放置處
  - scss # SCSS 的樣式放置處

- layout # ejs 模板放置處
- pages # 頁面放置處

- JavaScript 程式碼可寫在 main.js 檔案

### 注意事項

- 已將 pages 資料夾內的 index.html 預設為首頁，建議不要任意修改 index.html 的檔案名稱
- .gitignore 檔案是用來忽略掉不該上傳到 GitHub 的檔案（例如 node_modules），請不要移除 .gitignore

## 開發模式的監聽

vite 專案執行開發模式 `npm run dev` 後即會自動監聽，不需要使用 `Live Sass Compiler` 的 `Watch SCSS` 功能

## 部署 gh-pages 流程說明

### Windows 版本

1. 在 GitHub 建立一個新的 Repository

2. 部署前請務必先將原始碼上傳到 GitHub Repository 也就是初始化 GitHub，因此通常第一步驟會在專案終端機輸入以下指令

```cmd
git init # 若已經初始化過就可以不用輸入
git add .
git commit -m 'first commit'
git branch -M main
git remote add origin [GitHub Repositories Url]
git push -u origin main // 僅限第一次輸入，往後只需要輸入 git push
```

3. 初始化完畢後，執行 `npm run deploy` 指令進行自動化部署

## 提供資料

- github repo：
- github pages：

## 其他注意

- 在 vite.config.js 更改 base: '/Repository 的名稱/'
- 在 vite.config.js 更改 server 時預設開啟的頁面

- 第二次之後更新
- npm run dev
- git add .
- git commit -m 'first commit'
- git push
- npm run deploy

## 組長

- 建立工作平台，並將其他人加入進去
- cd [資料夾位置]
- git clone [將雲端資料下載在哪個資料夾]

---

- 組長接收到 pull requests
- 到 Sourcetree，main，看有沒有分支
- 沒有就可以 git fetch origin [需要審核分支名稱/name]
- 確認 git checkout [commit(推分支者代號)]
- 確認完畢，回到 git checkout main
- git merge origin main (本地合併最新的 main)
- git fetch origin main (遠端合併最新的 main)

---

## 組員 (協作)

- git clone [GitHub Repositories Url] //下載資料
- cd [剛剛下載並且要協作的資料夾]
- git checkout -b [分支名稱/name] //新增分支
- 開始開發
- git add .
- git commit -m 'first commit'
- git push origin [分支名稱/name]
- 發 PR，到 github，pull requests>New pull requests>點擊自己的[分支名稱/name]>create pull requests>註解>create pull requests

---

main 有更新

- git fetch origin main (遠端最新的 main)
- git merge origin main (本地端也要到最新的 main)

---

當 main 分支有不同基礎時

- git fetch origin main (遠端最新的 main)
- git rebase origin main (讓自己的新分支在最新的本地 main 上)
- git push origin [分支名稱/name]
- 發 PR，到 github，pull requests>New pull requests>點擊自己的[分支名稱/name]>create pull requests>註解>create pull requests
