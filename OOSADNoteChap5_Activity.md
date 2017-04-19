# Unit 5 活動圖 (Activity Diagram)

> **物件導向式的流程圖** <br>
> 描述流程中主要活動與各活動彼此間的關係<br>
> 多個邊(edge)與節點(node)相互所構成的活動流程 

![Activity](images/Activity2.PNG "Activity")

### 節點(node)
1.  動作節點 (Action node)
    > 活動裡不可分割的工作單元

    * 動作 (action) ： 簡單不可分割行為
    * 活動 (activity) ： 一組動作

    ![ActivityNode](images/ActivityNode.PNG "ActivityNode")

2.  控制節點 (Control node)
    > 控制整個活動流程

    ![ControlNode](images/ControlNode.PNG "ControlNode")

    * 開始節點 (Initial Node) ： 活動開始
    * 活動結束節點 ( activity-final node) ： 用來停止活動的所有`物件流`及`控制流`
    * 流程結束節點 (flow-final node) ： 用來停止特定活動的`物件流`及`控制流`
    * 決策節點 (decision node) ： 根據條件走訪路徑
         > 標示門檻條件(guard condition) ： 走訪這條路徑的測試值

    * 合併節點 (merge node) ： 會合`決策節點`導致的分叉路徑

        ![DecisionMerge](images/ControlNode_DMN.PNG "DecisionMerge")
        ![DecisionMerge](images/ControlNode_DMN2.PNG "DecisionMerge")

    * 分叉節點 (fork node) ： 將流程分割成數個併行或平行流程
        > 泳道 (又稱`活動段落` ， Swimlane)： 辨識活動圖的分解 ， 易於閱讀

    * 連接節點 (join node) ： 會合平行或併行流程

        ![ForkJoin](images/ControlNode_FJ.PNG "ForkJoin")

3. 物件節點 (Object node)
    > 活動裡使用的物件 <br>
    > 代表從一個活動流程到另一個活動的資訊

    ![ObjectNode](images/ObjectNode2.PNG "ObjectNode")

    * 緩衝區
        > 等待被其他節點接受

        * 定義緩衝區如何運作 

            ![ObjectNode_Buffer](images/ObjectNode_Buffer.PNG "ObjectNode_Buffer")
            
        * 選擇行為

            > 條件附加於節點選擇輸入邊的物件形成

            ![ObjectNode_Buffer](images/ObjectNode_Buffer2.PNG "ObjectNode_Buffer")

    * 表現物件狀態 `[ ]`
        > 時空的停頓

        ![ObjectNode_State](images/ObjectNode_State.PNG "ObjectNode_State")

    * 參數 `( )`
        > 活動的輸入輸出窗口 <br>
        > 繪製位置必須與框重疊

        ![ObjectNode_Param](images/ObjectNode_Param.PNG "ObjectNode_Param")

### 邊(edge)
1. 控制流程 (control flow)
    > 活動控制權的流向

2. 物件流程 (object flow)
    > 物件裡物件的流向 <br>
    > 物件的輸入與輸出

    ![ObjectFlow](images/ObjectFlow2.PNG "ObjectFlow")

### 黑洞活動 (black hole activities)
> 沒有流出的活動

### 奇蹟活動 (miracle activity)
> 沒有流入的活動

### 活動段落
> 讓活動圖易於閱讀

![Swimlane](images/Activity_Swimlane.PNG "Swimlane")

### 連接點 (connector)
> 避免 `edge` 交錯複雜

![Connector](images/Activity_Connector.PNG "Connector")

### 可中斷活動區 (Interruptible Activity Region)
> 當有中斷訊息發生即可中斷活動區域

![IAR](images/Activity_IAR.PNG "IAR")

#### 中斷訊號 
![IS](images/Activity_IS.PNG "IS")
![IS2](images/Activity_IS2.PNG "IS2")

### 腳位 (PIN)
> `object note` <br>
> 放置在`動作 (action)`的輸入或輸出，一個輸入對一個輸出

![PIN](images/Activity_PIN.PNG "PIN")

### 擴充節點 (Expansion Node)
> object note <br> 
> 表現出擴充區是如何處理一組物件之集合

#### 擴充區 (Expansion)
* 反覆式(Iterative) 
    > 依序處理集合內的每個元件
* 平行式(Parallel) 
    > 平行處理集合內的每個元件
* 串流式(Stream) 
    > 依元件到達順序處理集合內的每個元件


![ExpansionNode](images/Activity_ExpansionNode.PNG "ExpansionNode")

#### 串流
> 依元件到達順序處理集合內的每個元件

![Stream](images/Activity_Stream.PNG "Stream")

> 標頭為填滿黑色：signal，無資料 <br>
> 標頭無填滿：message，有資料

### 系統徵求書 (Request for proposal ， RFP)
> 組織為了制定標準所採用的建議書徵求流程

### 參數組合 (Parameter Set)
> 可以組合不同的輸入輸出`角位(PIN)` <br>
> 輸入不能與輸出組合

![PS](images/Activity_ParameterSet.PNG "PS")

### 輸入(input effect)、輸出(output effect)影響
> 輸入輸出時造成的影響 <br>
> 可以用大括弧包住說明內容

![IOE](images/Activity_IOE.PNG "IOE")
----

## 補充

### Node 

| 名稱(中文) | 名稱(英文) | 用途 | 圖示 | 備註 |
|---|---|---|---|---|
| 動作 | action | 簡單不可分解的行為| ![Action](images/ActionNode_Action.PNG "Action") | Action Node |
| 活動 | activity | 一組動作 | ![Activity](images/ActionNode_Activity.PNG "Activity")  ![Activity](images/ActionNode_Activity2.PNG "Activity")  | Action Node |
| 物件節點 | object node | 代表從一個活動流程到另一個活動的資訊 | ![Object](images/ObjectlNode.PNG "Object") | Object Node |
| 開始節點 | Initial Node |  活動開始 |  ![IN](images/ControlNode_IN.PNG "IN") | Control Node  |
| 活動結束節點 |  activity-final node |  用來停止活動的所有`物件流`及`控制流` | ![AFN](images/ControlNode_AFN.PNG "AFN") |   Control Node |
| 流程結束節點 | flow-final node | 用來停止特定活動的`物件流`及`控制流` | ![FFN](images/ControlNode_FFN.PNG "FFN") | Control Node |
| 決策節點 | decision node | 根據條件走訪路徑 |  ![DN](images/ControlNode_DN.PNG "DN")  ![DN](images/ControlNode_DN2.PNG "DN") | `OR` 關係 <br> Control Node |
| 合併節點 | merge node | 會合`決策節點`導致的分叉路徑 | ![MN](images/ControlNode_MN.PNG "MN")  ![MN](images/ControlNode_MN2.PNG "MN")  | `OR` 關係 <br> Control Node |
| 分叉節點 | fork node |  將流程分割成數個併行或平行流程 | ![Fork](images/ControlNode_Fork.PNG "Fork")  | `AND` 關係 <br> Control Node |
| 連接節點 | join node | 會合平行或併行流程 | ![Join](images/ControlNode_Join.PNG "Join")  | `AND` 關係 <br> Control Node |
| 控制流程 | control flow | 活動控制權的流向 | ![CF](images/ControlFlow.PNG "CF") | edge |
| 物件流程 | object flow | 物件裡物件的流向 |  ![OF](images/ObjectFlow.PNG "OF")  | edge |


#### Action Node

| 名稱 | 用途 | 圖示 | 
|---|---|---|
| 呼叫動作節點 | 呼叫活動、系統行為或動作 |  ![CAN](images/ActionNode_CAN.PNG "CAN") |
| 傳送訊號 | 「產生」某一個特定的信號<br> 傳送非同步訊號，可接收輸入參數 | ![SS](images/ActionNode_SS.PNG "SS")  |
| 接收事件動作節點 | 「等待」某一個特定事件發生 |  ![RAN](images/ActionNode_RAN.PNG "RAN")  |
| 接收時間事件動作節點 | 對時間事件的回應 <br> 因為有時我們需要等待一段時間後，才會進行下一個動作，或周期定時執行一些動作  |  ![TE](images/ActionNode_TE.PNG "TE")  |

#### Object Node

| 名稱 | 用途 | 圖示 | 
|---|---|---|
| 腳位 | 放置在`動作 (action)`的輸入或輸出，一個輸入對一個輸出 | ![PIN](images/Activity_PIN2.PNG "PIN") |
| 擴充節點 | 表現出擴充區是如何處理一組物件之集合 | ![ExpansionNode](images/Activity_ExpansionNode2.PNG "ExpansionNode") |


### \<\< \>\> Stereotype

> 具有相同型式(如相同的屬性與關係)的現有模組元件的變化，但這些變化指示修改一些語意的部分

| 名稱 | 用途 | 
|---|---|
| \<\<external\>\> | 活動圖與外部系統溝通 <br> 外部活動段落並非系統一部份 |
| \<\<selection\>\> | 物件流程中的條件說明<br>僅接收滿足的條件 |
| \<\<transformation\>\> | 物件流程中物件轉換成不同的類型 |
| \<\<multicast\>\> | 多方傳遞<br>物件傳遞給多個接收者 |
| \<\<multireceive\>\> | 多方接收<br>物件從多個地方傳遞而來 |
| \<\<centralbuffer\>\> | 輸出與輸入間的緩衝區 |

![MutilCS](images/ActivityStereotype_CS.PNG "MutilCS")
![centralbuffer](images/ActivityStereotype_C.PNG "centralbuffer")

### 其他
* :: 
    > 分隔活動段落

* ( , ) 
    > 標明活動在活動段落架構下的位置，若活動分布於一格以上段落，我們以逗號分隔活動段落。

    ![Activity_Paragraph](images/Activity_Paragraph.PNG "Activity_Paragraph")
* 耙子符號(Rake) 
    > 代表動作呼叫某個活動，節點名稱與呼叫的活動相同

    ![Rake](images/Rake.PNG "Rake")

* ( )
    > 參數

* [ ] 
    > condition , state

* { } 
    > constraint (強限制) , tagged value (弱限制，標記值)

* Note / Artifact 

![Note](images/Note.PNG "Note")
