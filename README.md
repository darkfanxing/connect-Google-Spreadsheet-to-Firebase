# Firebase + Spreadsheet

> reference：https://medium.com/firebase-developers/sheets-to-firebase-33132e31935b

upload data of Google Spreadsheet to Firebase Realtime database

1. setup Firebase project
2. setup Realtime Database on firebase, get project's URL
    ![img/Untitled.png](img/Untitled.png)

3. change rule and deploy on the following page:
    ![img/Untitled%201.png](img/Untitled%201.png)

4. check the data type of Google Spreadsheet is as following image:
    ![img/Untitled%202.png](img/Untitled%202.png)

5. open script editor
    ![img/Untitled%203.png](img/Untitled%203.png)

6. change the filename: `程式碼.gs` to [code.gs](https://github.com/darkfanxing/connect-spreadsheet-to-firebase/blob/master/code.gs) and change two parameters:
    ![img/Untitled%204.png](img/Untitled%204.png)

    - spreadsheetID：
        - spreadsheetID is here: [https://docs.google.com/spreadsheets/d/{spreadsheetID}](https://docs.google.com/spreadsheets/d/1nbot7akhbB6exTWWSkzx3ogGEHJM0l-YLWQD2o2iH5c/edit?pli=1#gid=63193665)<your-spreadsheet-id>
    - firebaseUrl：
        - fill the Firebase project's URL on step 2

7. open View > Show file list on script editor
    ![img/Untitled%205.png](img/Untitled%205.png)

8. you can find the `appsscript.json` file on the left sidebar now，copy this [appsscript.json](https://github.com/darkfanxing/connect-spreadsheet-to-firebase/blob/master/appsscript.json) and paste on your `appsscript.json` file
9. Open Execute > execute function > initialize on script editor
    ![img/Untitled%206.png](img/Untitled%206.png)
    
now, you can upload some data to Firebase!

Finally，if you don't want to the data exposure to a dangerous enviroment, you can change it as the following parameters on rule page
![img/Untitled%207.png](img/Untitled%207.png)

the format of data on Firebase after uploaded
![img/Untitled%208.png](img/Untitled%208.png)
