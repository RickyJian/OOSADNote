# Unit 8 狀態機 (State Machine)

![StateMachine](images/StateMachine_TopGround.PNG "StateMachine")

* 描述系統動態行為
* 被動物件生命週期
* 每個類別有多個狀態機

## 狀態

物件在其生命中因滿足某些條件、展現某些活動或等待某些事件時的一個條件或情況

> 被動物件：
> * 會回應外部事件(物件本體之外的事件)
> * 會產生與回應內部的事件
> * 會用一連串的狀態、轉換與事件來描述生命週期
> * 現在的行為是依據過去的行為而生

## 事件

時空間中發生的事項

## 傳換

反應事件過程中從一個狀態移動到另一個狀態

## 行為狀態機 (Behavioral State Machine)

定義類詞行為，用來描述類詞部分的行為，但有些類詞是沒有行為的，例：介面、連接埠，指定義使用使用協定。

### 狀態

一個或多個進入(Entered)、停留(Resided in)、或離開(Exited)狀態時的動作

## 協定狀態機(Protocol State Machine)

定義類詞中的協定，例：呼叫類詞及其實例動作後的狀態、呼叫動作後的結果、呼叫動作的順序。不會定義實作內容，僅定義面對外部實體時該如何表現

### 狀態

不會指明任何動作

## 圖示語意

圖稱(中文) | 圖稱(英文) | 語意 | 圖示
---------|----------|---------- | ----------
初始狀態 | Initail Start State | 狀態起始 | ![InitailStartState](images/StateMachine_InitailStartState.PNG "InitailStartState")
結束狀態 | Stop State | 狀態結束 |  ![StopState](images/StateMachine_StopState.PNG "StopState")
轉換 |  | 狀態改變，只含箭頭 | ![Transform](images/StateMachine_Transform.PNG "Transform")
事件 |  | 時空間中發生的事項，傳換箭頭上方 | ![Transform](images/StateMachine_Transform.PNG "Transform")