# [107-2] Web Programming Final - Fashion Ceiba
This project was developed by [JacksonHsieh](https://github.com/hsiehjackson), [CynthiaYLiu](https://github.com/CynthiaYLiu), and [PierreSue](https://github.com/PierreSu). You can view this project on the browser through the following link [Fashion-Ceiba](http://fashion-ceiba.herokuapp.com/login) and see the demonstration video by opening [Demo-video](TODO放連結).
<img src="https://imgur.com/s3AY3au" alt="drawing"/> 

## 題目名稱/一句話描述這個 project 在做什麼
```
$ 題目名稱 : (Group 03) Fashion Ceiba
$ 組員：解正平(B04901020)、劉芸欣(B04901152)、蘇峯廣(B04901070)
$ project 描述：一個課程教學平台，用於輔助教學系統，即時筆記、發問、更新上課講義。
```
## Deployed 連結
```
http://fashion-ceiba.herokuapp.com/login
```
## 安裝/使用/操作方式
```
$ From Github:
    * git clone https://github.com/hsiehjackson/fashion-ceiba
    * change the MONGODB link in ./fashion-ceiba/.env
    * npm install (./fashion-ceiba/)
    * npm run server (./fashion-ceiba/)  - port:4000
    * npm run client1 (./fashion-ceiba/) - port:3000
    * npm run client2 (./fashion-ceiba/) - port:3001
    * If you want to use teacher mode, just sing up with name/email/pwd ADMIN
$ From Deployed Link:
    * open http://fashion-ceiba.herokuapp.com/login
    * and enjoy
```
畫面一開始為登入介面，可以進行註冊或者是登入，若以(name/email/pwd == ADMIN/ADMIN/ADMIN)登入即為老師模式，其他皆為學生模式。進入下一個畫面以後，除了基本的ceiba功能以外，多加了上傳pdf(Upload pdf)的功能，可以進行瀏覽編輯，更可以像簡報一樣繪畫註記，另外同步上，所有學生可以收到老師的即時編輯，也可以在自己的pdf上新增筆記，而不會影響到其他用戶。此外，為了增進上課互動，還新增了聊天室功能，所有人可以即時收到訊息通知，知道其他同學對那些地方有疑問，老師也可以收到問題並將疑問加到投影片內。


## 其他說明
* Upload Large Files: 因為我們的PDF可能檔案過大，所以要處理從client傳到server端，還有server端傳到database的問題。其中從client傳到server端要使用apollo-upload來將檔案切成一個filestream傳，並且要提高上限。再來server傳到client端要使用GridFS來解決mogodb只能上傳上限16mb的問題，將檔案切成小檔案再存到database中。
* 

## 使用與參考之框架/模組/原始碼
```
1. https://github.com/daisy3607/react-sketch
2. https://github.com/wojtekmaj/react-pdf
3. https://github.com/lykmapipo/mongoose-gridfs
```
## 專題製作心得
* 解正平：做完project最有成就感的地方就是終於看懂老師之前上的一張圖，從database一路連貫到browser的過程都很清楚，其中使用graphQL的能力也大大提升。

## 使用之第三方套件、框架、原始碼
```
* mongodb/mongoose/mongoose-gridfs
* node.js
* express.js
* graphql-yoga
* react-apollo
* react-sketch
* react-pdf
* node-sass
* react.js
```
## Demo 影片連結
[TODO放連結](TODO放連結)

## 每組組員的貢獻
```
$ 解正平(B04901020)
    * Authetication/Ceiba基本功能/upload pdf 之 介面/前端/後端/資料庫
    * Deploy 在 herokuapp

$ 劉芸欣(B04901152)
    * Sketchboard 之 介面/前端/後端/資料庫
    * 影片剪輯

$ 蘇峯廣(B04901070)
    * Chatroom 之 介面/前端/後端/資料庫
```

## 對於此課程的建議
* 建議上課之前可以先創好每次作業要使用的檔案，同學也可以直接跟著範例上課。
