# Unit 8 狀態機 (State Machine)

* 描述系統動態行為
* 被動物件生命週期
* 每個類別有多個狀態機

![StateMachine](images/StateMachine_TopGround.PNG "StateMachine")

## 狀態

物件在其生命中因滿足某些條件、展現某些活動或等待某些事件時的一個條件或情況，隨著時間的改變，物件狀態也會改變，不過在特定的時間點上物件也會中止，中止原因：物件的屬性值、和其他物件的關係、物件展現得活動。

> 被動物件：
> * 會回應外部事件(物件本體之外的事件)
> * 會產生與回應內部的事件
> * 會用一連串的狀態、轉換與事件來描述生命週期
> * 現在的行為是依據過去的行為而生

## 事件

時空間中發生的事項

## 轉換

反應事件過程中從一個狀態移動到另一個狀態

### 內部轉換

描述模型中雖然有發生某些事情但是並沒有觸發任何的狀態的轉換，是由於不夠重要

## 行為狀態機 (Behavioral State Machine)

定義類詞行為，用來描述類詞部分的行為，但有些類詞是沒有行為的，例：介面、連接埠，指定義使用使用協定。

### 狀態

一個或多個進入(Entered)、停留(Resided in)、或離開(Exited)狀態時的動作

#### 動作(Action)與活動(Activity)

* 每個狀態機中都包含0個以上動作(Action)與活動(Activity)
* 動作(Action)：花費時間瞬間且不可中斷
* 活動(Activity)：花費時間一段時間且是可以中斷

 ![Action](images/StateMachine_Action.PNG "Action")


### 轉換

簡單語法表示

* 零個以上的事件：指名哪些可以觸發的外部或內部事件
* 零個或一個判斷條件：布林算表示式，true才會發生狀態轉換
* 零個以上的Action：一連串與轉換相關的作業，且發生在轉換開始的瞬間

#### 外部

箭頭線條表示

#### 內部

顯示在狀態內部`*`

## 協定狀態機(Protocol State Machine)

定義類詞中的協定，例：呼叫類詞及其實例動作後的狀態、呼叫動作後的結果、呼叫動作的順序。不會定義實作內容，僅定義面對外部實體時該如何表現

### 狀態

不會指明任何動作

### 轉換

判斷條件由前置條件(Precondition)與後置(Postcondition)所取代

## 圖示語意

圖稱(中文) | 圖稱(英文) | 語意 | 圖示
---------|----------|---------- | ----------
初始狀態 | Initail Start State | 狀態起始 | ![InitailStartState](images/StateMachine_InitailStartState.PNG "InitailStartState")
結束狀態 | Stop State | 狀態結束 |  ![StopState](images/StateMachine_StopState.PNG "StopState")
轉換 |  | 狀態改變，只含箭頭 | ![Transform](images/StateMachine_Transform.PNG "Transform")
事件 |  | 時空間中發生的事項，傳換箭頭上方 | ![Transform](images/StateMachine_Transform.PNG "Transform")