# Unit 5 活動圖 (Activity Diagram)

> **物件導向式的流程圖** <br>
> 描述流程中主要活動與各活動彼此間的關係<br>
> 多個邊(edge)與節點(node)相互所構成的活動流程 

![InitialNode](images/Activity2.png "InitialNode")

### 節點(node)
1.  動作節點 (Action node)
    > 活動裡不可分割的工作單元

    * 動作 (action) ： 簡單不可分割行為
    * 活動 (activity) ： 一組動作

    ![Activity](images/Activity.png "Activity")

2.  控制節點 (Control node)
    > 控制整個活動流程

    ![ControlNode](images/ControlNode.png "ControlNode")

    * 開始節點 (Initial Node) ： 活動開始
    * 活動結束節點 ( final-activity node) ： 用來停止活動的所有`物件流`及`控制流`
    * 流程結束節點 (flow-final node) ： 用來停止特定活動的`物件流`及`控制流`
    * 決策節點 (decision node) ： 根據條件走訪路徑
         > 標示門檻條件(guard condition) ： 走訪這條路徑的測試值

    * 合併節點 (merge node) ： 會合`決策節點`導致的分叉路徑

        ![DecisionMerge](images/ControlNode_DMN.png "DecisionMerge")
        ![DecisionMerge](images/ControlNode_DMN2.png "DecisionMerge")

    * 分叉節點 (fork node) ： 將流程分割成數個併行或平行流程
        > 泳道 (又稱`活動段落` ， Swimlane)： 辨識活動圖的分解 ， 易於閱讀

    * 連接節點 (join node) ： 會合平行或併行流程

        ![ForkJoin](images/ControlNode_FJ.png "ForkJoin")

3. 物件節點 (Object node)
    > 活動裡使用的物件 <br>
    > 代表從一個活動流程到另一個活動的資訊

    ![ObjectNode](images/ObjectNode2.png "ObjectNode")

    * 緩衝區
        > 等待被其他節點接受

        * 定義緩衝區如何運作 

            ![ObjectNode_Buffer](images/ObjectNode_Buffer.png "ObjectNode_Buffer")
            
        * 選擇行為

            > 條件附加於節點選擇輸入邊的物件形成

            ![ObjectNode_Buffer](images/ObjectNode_Buffer2.png "ObjectNode_Buffer")

    * 表現物件狀態 `[ ]`
        > 時空的停頓

        ![ObjectNode_State](images/ObjectNode_State.png "ObjectNode_State")

    * 參數 `( )`
        > 活動的輸入輸出窗口 <br>
        > 繪製位置必須與框重疊

        ![ObjectNode_Param](images/ObjectNode_Param.png "ObjectNode_Param")

### 邊(edge)
1. 控制流程 (control flow)
    > 活動控制權的流向

2. 物件流程 (object flow)
    > 物件裡物件的流向 <br>
    > 物件的輸入與輸出

    ![ObjectFlow](images/ObjectFlow2.png "ObjectFlow")

### 黑洞活動 (black hole activities)
> 沒有流出的活動

### 奇蹟活動 (miracle activity)
> 沒有流入的活動

### 活動段落
> 讓活動圖易於閱讀

![InitialNode](images/Activity_Swimlane.png "InitialNode")

----
## 補充

### Node 

| 名稱(中文) | 名稱(英文) | 用途 | 圖示 | 備註 |
|---|---|---|---|---|
| 動作 | action | 簡單不可分解的行為| ![Action](images/Action.png "Action") | Action Node |
| 活動 | activity | 一組動作 | ![Activity](images/ActionNode_Activity.png "Activity")  ![Activity](images/ActionNode_Activity2.png "Activity")  | Action Node |
| 物件節點 | object node | 代表從一個活動流程到另一個活動的資訊 | ![Object](images/ObjectlNode.PNG "Object") | Object Node |
| 開始節點 | Initial Node |  活動開始 |  ![IN](images/ControlNode_IN.png "IN") | Control Node  |
| 活動結束節點 |  activity-final node |  用來停止活動的所有`物件流`及`控制流` | ![AFN](images/ControlNode_AFN.png "AFN") |   Control Node |
| 流程結束節點 | flow-final node | 用來停止特定活動的`物件流`及`控制流` | ![FFN](images/ControlNode_FFN.png "FFN") | Control Node |
| 決策節點 | decision node | 根據條件走訪路徑 |  ![DN](images/ControlNode_DN.png "DN")  ![DN](images/ControlNode_DN2.png "DN") | `OR` 關係 <br> Control Node |
| 合併節點 | merge node | 會合`決策節點`導致的分叉路徑 | ![MN](images/ControlNode_MN.png "MN")  ![MN](images/ControlNode_MN2.png "MN")  | `OR` 關係 <br> Control Node |
| 分叉節點 | fork node |  將流程分割成數個併行或平行流程 | ![Fork](images/ControlNode_Fork.png "Fork")  | `AND` 關係 <br> Control Node |
| 連接節點 | join node | 會合平行或併行流程 | ![Join](images/ControlNode_Join.png "Join")  | `AND` 關係 <br> Control Node |
| 控制流程 | control flow | 活動控制權的流向 | ![CF](images/ControlFlow.png "CF") | edge |
| 物件流程 | object flow | 物件裡物件的流向 |  ![OF](images/ObjectFlow.png "OF")  | edge |


#### Action Node

| 名稱 | 用途 | 圖示 | 
|---|---|---|
| 呼叫動作節點 | 呼叫活動、系統行為或動作 |  ![CAN](images/ActionNode_CAN.png "CAN") |
| 傳送訊號 | 「產生」某一個特定的信號<br> 傳送非同步訊號，可接收輸入參數 | ![SS](images/ActionNode_SS.png "SS")  |
| 接收事件動作節點 | 「等待」某一個特定事件發生 |  ![RAN](images/ActionNode_RAN.png "RAN")  |
| 接收時間事件動作節點 | 對時間事件的回應 <br> 因為有時我們需要等待一段時間後，才會進行下一個動作，或周期定時執行一些動作  |  ![TE](images/ActionNode_TE.png "TE")  |


* :: 
    > 分隔活動段落

* ( , ) 
    > 標明活動在活動段落架構下的位置，若活動分布於一格以上段落，我們以逗號分隔活動段落。

    ![InitialNode](images/Activity_Paragraph.png "InitialNode")
* 耙子符號(Rake) 
    > 代表動作呼叫某個活動，節點名稱與呼叫的活動相同

    ![Rake](images/Rake.png "Rake")

*  \<\<external\>\>
> 活動圖與外部系統溝通 <br>
> 外部活動段落並非系統一部份

* ( )
    > 參數

* [ ] 
    > condition , state

* { } 
    > constraint (強限制) , tagged value (弱限制，標記值)

