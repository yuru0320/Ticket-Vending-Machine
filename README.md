# Ticket-Vending-Machine

# 開發平台
Window 10

# 開發環境
ModelSim-Altera 10.1d (Quartus II 13.1)

# 使用流程
1.以ModelSim開啟vending_machine.n以及stimulus.v並編譯

2.對stimulus.v進行模擬

# 說明
利用有限狀態機的方法模擬出車票販賣機，分為四個狀態: 選擇車站、選擇張數、付款、找零及給票。

<img width="327" alt="image" src="https://user-images.githubusercontent.com/95215851/191296655-7378a83b-36a3-4661-b6b8-6ce3ae59abe3.png">

* 首先要輸入兩個站（起站與終站）// 初始狀態

* 接著輸入張數 // 選擇張數的狀態

* 開始投錢 （此時要顯示已投入多少錢以及還欠缺多少錢）// 付款狀態

* 當錢的數量足夠時輸出找零和票數（此時要顯示須找多少錢以及票數）// 結帳狀態

* 當退幣(reset)時，必須退出所有已輸入的零錢 回到初始的狀態（選站) // 取消買票

* 可以投入零錢種類為1元、5元、10元、50元 ( 不可同時投入多個硬幣，例如: 一次投入2個1元 )

* 票數的選擇為 1～5張 

* 車站為 S1、S2、 S3、S4、S5 共五站

* 選站時必須選擇“起點站”與“終點站”

* 當起站與終站相同時則為”月台票”

<img width="678" alt="image" src="https://user-images.githubusercontent.com/95215851/191297466-ce274983-06c8-4157-ae16-52af6fb4da5e.png">

# Input 說明
origin: 起始站

destination: 目的站

howManyticket: 車票張數

money: 投入金額

reset: 取消


![messageImage_1665057803737](https://user-images.githubusercontent.com/95215851/194366806-1dac43fb-a6fc-4751-9ea2-a7cbc235f577.jpg)

# Output 說明
money: 投入金額
total dollars: 已投入金額
Amount payable: 還需付多少錢
exchange: 取消後退還多少錢
Change: 結帳完成後找零金額
Ticket num: 車票數量

![messageImage_1665057752116](https://user-images.githubusercontent.com/95215851/194366887-e8b845cb-b7d5-4aa8-8425-cb1b5b69dac4.jpg)


