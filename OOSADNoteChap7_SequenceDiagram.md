# Unit 7 循序圖 (Sequence Diagram)

生命線之間事件發生的先後順序

![Sequence](/images/Sequence_TopGround.PNG "Sequence") 

![Sequence](/images/Sequence_TopGround2.PNG "Sequence") 

## 啟動 (Activation)

又稱控制焦點(Focus Of Control)

## 註解

說明圖中意義

## 狀態不變量 (State Invariant)

當實例收到訊息，可能會改變其狀態(State)。當沒有不良邊際效益是不會改變實例狀態。

> 狀態：物件在生命周期時能滿足某些要求、執行某些活動，或等待某些事件的條件或情況

## 限制 (Constraint)

表示該實例往後必須滿足此限制

![State Invariant](/images/Sequence_StateInvariant.PNG "State Invariant") 

## 符號

名稱 | 定義 | 符號
---------|----------|---------
參與者 | 人或系統能從系統獲益且置身於系統之外<br>透過訊息收發，參與某個協力合作 | ![Actor](/images/Sequence_Actor.PNG "Actor") ![Actor](/images/Sequence_Actor2.PNG "Actor") 
物件 | 透過訊息收發，參與某個協力合作 | ![Actor](/images/Sequence_Object.PNG "Actor")
生命線 | 代表物件在序列期間的生命<br>不再互動的地方包含一個X符號 | ![LifeLine](/images/Sequence_LifeLine.PNG "LifeLine")
執行事件 | 標示出物件何時收發訊息 | ![ex](/images/Sequence_Execution.PNG "ex")
訊息 | 訊息從物件傳到另一個物件<br>傳送：實現箭頭<br>回傳：虛線箭頭 | ![Message](/images/Sequence_Message.PNG "Message")