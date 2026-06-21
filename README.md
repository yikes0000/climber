# Contact Sheet — Flickr 相簿存底工具

純前端的小工具，貼上 Flickr 公開相簿網址，瀏覽縮圖、選畫質、下載。
全部運算都在瀏覽器本機執行，不經過任何伺服器，沒有登入機制。

## 放上 GitHub Pages（個人用）

1. 在 GitHub 開一個新的 repository（可以設成 Private，純自己用的話沒差）。
2. 把 `index.html` 上傳到這個 repo 的根目錄。
3. 進 repo 的 **Settings → Pages**。
4. Source 選 **Deploy from a branch**，Branch 選 `main` / `/(root)`，按 Save。
5. 等個一兩分鐘，GitHub 會給你一個網址，格式是：
   `https://你的帳號.github.io/repo名稱/`
6. 打開那個網址就能用了。

> 如果 repo 設成 Private，GitHub Pages 預設不會生效（要 Pro 帳號才能對 Private repo
> 開 Pages）。免費帳號的話，repo 設成 Public 才能用 Pages，但因為這個工具本身
> 不含任何密鑰或個人資料（API key 只存在你瀏覽器自己的 localStorage，不會進到
> 程式碼或 GitHub 上），repo 設 Public 也沒有資安問題。

## 使用方式

1. 第一次使用：打開頁面原始碼任意找一個 Flickr 相簿頁面的「api_key」字串
   （頁面內有「找不到 API Key？」的說明），貼到工具上方的欄位，瀏覽器會記住它。
2. 貼上想抓的相簿網址 → 按「載入相簿」。
3. 縮圖出現後，預設全選；可以點掉不要的，或按「全選 / 取消全選」切換。
4. 選好畫質（large / original / medium / small）→ 按「下載已選相片」。
5. 瀏覽器可能會跳出「這個網站要下載多個檔案」的提示，按允許即可逐張下載。

## 限制（平台端，非工具問題）

- 只能抓「公開」相簿。
- Flickr 對未登入訪客會自動過濾掉分級為 moderate 的相片，所以看到的張數
  可能比你登入瀏覽時看到的少。這是 Flickr 平台本身的規則，這個工具沒有
  登入機制，所以無法繞過（也不會嘗試繞過）。
