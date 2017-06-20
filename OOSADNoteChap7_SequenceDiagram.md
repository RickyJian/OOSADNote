# Unit 7 循序圖 (Sequence Diagram)

生命線之間事件發生的先後順序

![Sequence](/images/Sequence_TopGround.PNG "Sequence") 

![Sequence](/images/Sequence_TopGround2.PNG "Sequence") 

> 自我指派：物件自己呼叫自己

## 啟動 (Activation、Focus Of Control`、 Execution Occurrence)

又稱控制焦點(Focus Of Control)，互動片段，用來表現物件的開始與結束的執行過程。

## 生命線 

互動關係的參與者，有就是物件的互動關係

![Lifeline](/images/Sequence_Lifeline2.PNG "Lifeline") 

![Lifeline](/images/Sequence_Lifeline3.PNG "Lifeline") 

### 名稱

互動的生命線名稱

### 選擇器

滿足條件的實例的布林表示式

### 類型

類詞的實體名稱，也就是物件名稱

## 註解

說明圖中意義

## 狀態不變量 (State Invariant)

當實例收到訊息，可能會改變其狀態(State)。當沒有不良邊際效益是不會改變實例狀態。

> 狀態：物件在生命周期時能滿足某些要求、執行某些活動，或等待某些事件的條件或情況

## 限制 (Constraint)

表示該實例往後必須滿足此限制

![State Invariant](/images/Sequence_StateInvariant.PNG "State Invariant") 

## 符號

名稱(中) | 名稱(英) | 定義 | 符號
---------|----------|----------|---------
參與者 | participate | 人或系統能從系統獲益且置身於系統之外<br>透過訊息收發，參與某個協力合作 | ![Actor](/images/Sequence_Actor.PNG "Actor") ![Actor](/images/Sequence_Actor2.PNG "Actor") 
物件 | objec | 透過訊息收發，參與某個協力合作 | ![Actor](/images/Sequence_Object.PNG "Actor")
生命線 | lifeline | 代表物件在序列期間的生命<br>不再互動的地方包含一個X符號 | ![LifeLine](/images/Sequence_LifeLine.PNG "LifeLine")
執行事件 | Execution Occurrence <br> focus of control <br> activation  | 標示出物件何時收發訊息 | ![ex](/images/Sequence_Execution.PNG "ex")
訊息 | message | 訊息從物件傳到另一個物件<br>傳送：實現箭頭<br>回傳：虛線箭頭 | ![Message](/images/Sequence_Message.PNG "Message")

## 訊息

互動裡的兩條生命線互相船底訊息的媒介

* 呼叫動作—呼叫訊息
* 建立與消滅實例—建立與消滅訊息
* 傳送訊息(Signal)

名稱 | 語意 | 圖例
---------|----------|---------
同步訊息 | 傳送者等候接收者執行訊息完畢後回傳另一個訊息 | ![Sync](/images/Sequence_SyncMessage.PNG "Sync")
非同步訊息 | 傳送者傳送訊息後繼續執行—不等後接收者回傳訊息 |  ![aSync](/images/Sequence_AsyncMessage.PNG "aSync")
回傳訊息 | 接收回傳先前接收到的啟動信號 | ![return](/images/Sequence_ReturnMessage.PNG "return")
物件產生 | 傳送者建立接收者所指定的類詞實例 |  ![ObjectGenerate](/images/Sequence_ObjectGenerate.PNG "ObjectGenerate")
物件消滅 | 傳送者消滅接收者 |  ![ObjectDestroy](/images/Sequence_ObjectDestroy.PNG "ObjectDestroy")
發現訊息 | 傳送者訊息不再物件範圍內 |  ![MessageFound](/images/Sequence_MessageFound.PNG "MessageFound")
遺失訊息 | 訊息無法直接送達接收者 | ![MessageDisappeared](/images/Sequence_MessageDisappeared.PNG "MessageDisappeared")
