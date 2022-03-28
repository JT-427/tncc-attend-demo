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
當與會者到現場時，須出示QRCode或報到編號，工作人員（招待）透過Line或QRCode掃瞄器幫助與會者完成報到。
- QRCode  
利用Apple手機內建的app "[Shortcut](https://apps.apple.com/app/id1462947752)"來對Api送出Post請求。

- Line  
串接Line機器人([Line Bot](https://developers.line.biz/en/docs/messaging-api/overview/))，在特定聊天室中送出報到編號，即完成報到工作。  

- Telegram  
已成功串接[Telegram Bot](https://core.telegram.org/api)，但尚未設計回應模式。

- 手動登記  
點擊綠色勾勾完成點名，點擊紅色叉叉則取消出席紀錄。
![img](https://github.com/JT-427/tncc-attend-demo/blob/master/ex/rollcall.png)

#### *開發中*
- *串接Line和Telegram進行身份驗證：  
目前是用程式做出QRCode後，手動傳給每個人，但這樣會遇到有人沒有將QRCode存下來，以至於到現場時沒辦法提供QRCode，如果能串接通訊軟體，就可以讓與會者隨時透過通訊軟體取得自己的QRCode。*
- *寫一個掃描QRCode的app：  
目前使用Shortcut來掃描，但常常發生不穩定的狀況。不使用一般的掃描QRCode app是因為，目前沒有找到可以設定GET、POST方法、傳送value等功能之app。*

## 人數統計
彙整資料，並計算出席的人數、準時率、男女比......等資訊。
![img](https://github.com/JT-427/tncc-attend-demo/blob/master/ex/data.png)

***
### 專案開發期間
- 2021/9/11 ~  &nbsp;*(正式上線)*
- 2021/9/4 ~ 2021/9/5 &nbsp;*(上線測試)*
- 2021/8 ~ &nbsp;*(開發)*

