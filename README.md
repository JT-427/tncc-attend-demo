# 報到＆人數統計
> 此專案的目的是將舊有的紙本人數統計線上化，避免人為統計錯誤。  

> 在一場聚會中，會需要知道有多少人來，還有他們到的時間，並根據各個條件（ex:性別、年齡...）進行統計，計算出出席人數。過去的工作流程為，當有人入場時，工作人員需在單子上找到他的名字，並標記代號（ex:準時、遲到...），聚會結束後需要統整當天的出席人數，再依照各個條件統計，此方式容易出現人為錯誤（ex:不小心少算一個人），也很耗人力；因此想到，如果能讓工作人員只需要登記有誰出席，剩下的統計工作交給程式來處理，就可以省下非常多的時間和人力，因而開發此系統。

## Requirements
- python == 3.8
<!-- - [requirements.txt](https://github.com/JT-427/tncc-attend/blob/master/requirements.txt) -->

## Backend Framework
- [Flask](https://flask.palletsprojects.com/en/2.0.x/)

## DataBase
- [MySQL](https://www.mysql.com)

## Server
- [Linode](https://www.linode.com)

***

## 現場報到
當與會者到現場時，須出示QRCode，工作人員（招待）透過QRCode掃瞄器幫助與會者完成報到。
- QRCode  
原本是使用Apple手機內建的app [Shortcut](https://apps.apple.com/app/id1462947752) 來對Api送出Post請求，但不清楚是軟體bug還是有其他問題，導致與伺服器連線相當慢，因此決定自己寫一個app來處理掃描QRCode的工作。  
*app demo*  
![img](https://github.com/JT-427/tncc-attend-demo/blob/master/ex/app_demo.gif)

- 手動登記  
點擊綠色勾勾完成點名，點擊紅色叉叉則取消出席紀錄。  
![img](https://github.com/JT-427/tncc-attend-demo/blob/master/ex/rollcall.png)


## QRCode 取得方式
與會者入場時會使用到的QRCode可透過串接通訊軟體來取得。
|  |[Line Bot](https://developers.line.biz/en/docs/messaging-api/overview/) | [Telegram Bot](https://core.telegram.org/api) |
| :---- | :----: | :----: |
| 串接方式 | ![img](https://github.com/JT-427/tncc-attend-demo/blob/master/ex/line_connect.gif) | ![img](https://github.com/JT-427/tncc-attend-demo/blob/master/ex/telegram_connect.gif) |
| 取得方式 | 點擊圖文選單中的QRCode圖示 | 點擊左下角menu選單中的 "取得QRCode" |


## 人數統計
彙整資料，並計算出席的人數、準時率、男女比......等資訊。 
![img](https://github.com/JT-427/tncc-attend-demo/blob/master/ex/data.png)  


***
### 專案開發期間 

第二階段
- 正式上線: 2021/6/24 ~  
- 上線測試: 2022/6/18 ~ 2022/6/19 
- 開發: 2022/4 ~ 2022/6 

第一階段
- 正式上線: 2021/9/11 ~  
- 上線測試: 2021/9/4 ~ 2021/9/5 
- 開發: 2021/8 ~ 2022/1

