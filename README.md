# Firebase + Spreadsheet

將 Spreadsheet 的資料傳送到 Firebase Realtime database

1. 建立 Firebase project
2. 在 Firebase 中建立 Realtime Database，取得 project 的 Url

    ![img/Untitled.png](img/Untitled.png)

3. 進入到規則頁面，將安全性規則改為下列形式並發布：

    ![img/Untitled%201.png](img/Untitled%201.png)

4. 確認 spreadsheet 上的資料改為像下圖一樣的格式

    ![img/Untitled%202.png](img/Untitled%202.png)

5. 開啟指令編輯器

    ![img/Untitled%203.png](img/Untitled%203.png)

6. 將指令編輯器中的 `程式碼.gs` code 更改成 [code.gs](https://github.com/darkfanxing/connect-spreadsheet-to-firebase/blob/master/code.gs)，並更改兩樣參數

    ![img/Untitled%204.png](img/Untitled%204.png)

    - spreadsheetID：
        - 更改 spreadsheet 網址上的 id：[https://docs.google.com/spreadsheets/d/](https://docs.google.com/spreadsheets/d/1nbot7akhbB6exTWWSkzx3ogGEHJM0l-YLWQD2o2iH5c/edit?pli=1#gid=63193665)<your-spreadsheet-id>
    - firebaseUrl：
        - 更改成在第二步時，所取得的 Url
7. 在指令編輯器中打開 查看 > 顯示資訊清單檔案

    ![img/Untitled%205.png](img/Untitled%205.png)

8. 此時可以發現在左方欄位出現了 `appsscript.json` 的檔案，此時需要將其更改為 [appscript.json](https://github.com/darkfanxing/connect-spreadsheet-to-firebase/blob/master/appsscript.json)
9. 在程式編輯器中點開 執行 > 執行函式 > initialize

    ![img/Untitled%206.png](img/Untitled%206.png)

這時候就能成功的將資料傳送到 firebase 中了！

最後，如果不想將資料暴露在危險中，可以在規則頁面中，將安全性規則改為下圖並發布：

![img/Untitled%207.png](img/Untitled%207.png)

而傳送到 firebase 後，資料會像下圖的格式

![img/Untitled%208.png](img/Untitled%208.png)