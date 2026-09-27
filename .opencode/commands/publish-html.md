---
description: 產生 HTML、上傳到與專案同名的 GitHub repo、給連結並開啟
---

目標：產生一個 HTML 檔、上傳到與專案同名的 repository、給我連結網址並直接開啟。

固定參數：
- 專案目錄：`C:\opencode01`
- GitHub owner：`fox369788-rgb`
- Repo：`opencode01`（與專案同名）
- Branch：`main`，remote：`origin`
- GitHub Pages 已啟用（Branch `main` / `/ (root)`），渲染網址：`https://fox369788-rgb.github.io/opencode01/`

執行步驟（檔名用 $ARGUMENTS，若無則用 `index.html`）：
1. 在 `C:\opencode01\$ARGUMENTS` 產生 HTML，保留使用者指定的內文。
2. `git add` + `git commit` + `git push origin main`，確認 `git status -sb` 為 `main...origin/main` 且無待推。
3. 給三個連結並用 browser 開啟：
   - `https://github.com/fox369788-rgb/opencode01/blob/main/$ARGUMENTS`
   - `https://raw.githubusercontent.com/fox369788-rgb/opencode01/main/$ARGUMENTS`
   - `https://fox369788-rgb.github.io/opencode01/$ARGUMENTS`
4. 同時用 preview 開啟本地檔，讀出檔名、commit hash、遠端一致性後回報。
