# Unit 1 認識系統分析與設計

### 系統開發生命週期( System development life cycle ， SDLC )

> 了解及支援企業需要。 <br>
> 四個階段 ： 規劃、分析、設計與實作。


##### 階段( phase )

> 由許多的步驟( step ) 組成

#### 交付成果(deliverable)

> 了解專案成果與檔案

#### 規劃階段( planning phase ) 

> 為何建置系統 <br>
> 可行性分析 (feasibility analysis) <br>

####  可行性分析 (feasibility analysis)

> 技術可行性(T) <br>
> 經濟可行性(E) <br>
> 法律可行性(L) <br>
> 組織可行性(O) <br>
> 時程可行性(S) <br>

##### 經濟可行性(E) 

> Costing ： 
> 1. ABC ： Activity Based Costing
> 2. PBC ： Product Based Costing

#### 分析階段( analysis phase ) 

> who 、 what 、 where 、 when <br>
> 分析策略 (analysis strategy) 

##### 分析策略 (analysis strategy) 

> 分析現行系統(as-is) <br>
> 檢視新系統(to-be)

#### 設計階段( design phase ) 

> how <br>
> 架構設計、介面設計、資料庫與檔案規格、程式設計 <br>
> 此階段交付成果為`系統規格書 (system specification)`

#### 實作階段( implementation phase ) 

> 測試 、 安裝 、 訓練 、 支援

### 方法論( methodology )
> 實作 SDLC 的形式化方法 <br>
> step + deliverable <br>
> OOSAD ： 平衡 Process + data

#### 程序為主(process-centered)
> 程序、步驟、SOP

####  資料為主(data-centered)
> 資料、內容

#### 快速應用程式開發( rapid application development ， RAD )
> 階段式開發 (phased development) <br>
> 整個系統分成一系列版本(version)

### 物件導向系統設計與分析( Object-Oriented Systems Analysis and Design ， OOSAD )
> 方法論 ： 統一流程 <br>
> 圖面符號 ： 統以塑模語言
> 與 `RAD` 方法貼近

#### 使用案例導向 (Use-case driven)
> 專注於一項活動

##### 使用案例
> 定義系統行為

##### 案例描述 
> 使用者與系統相互作用

#### 以架構為中心 (Architecture centric)
> 逐步形成系統規格 <br>

##### 功能(外部觀點，functional view )
> 使用者觀點描述系統行為

##### 結構(靜態觀點，structural or static view )
> 屬性 、 方法 、 類別 、 關係描述系統結構

##### 動態觀點(dynamic view)
> 物件間所傳遞的訊息 <br>
> 物件內狀態的改變 <br>
> 描述系統內部行為

#### 反覆性(iterative)及漸進性 (incremental)
> `SDLC`中持續進行測試及細部調整

### 統一流程(Unified Process)
> 方法論，定義使用UML技術

### 統一塑模語言 (Unified Modeling Language，UML)
> 14 個製圖技巧 <br>
> Diagrams = Things + Relationships

#### 結構圖(Structure Diagrams) 
> 資料靜態關係

| 圖稱(中文) | 英文 | 用途 | 主要階段 |
| ---- | --- | ---| ---|
| 類別 | Class Diagram | 系統中類別模型之間的關係 | 分析、設計
| 物件 | Object Diagram | 系統中物件模型之間的關係 。 類別實例 | 分析、設計 |
| 套件 | Package Diagram | UML元素組成 | 分析、設計、實作 |
| 部屬 | Deployment Diagram | 顯示系統實體架構 | 分析、設計、實作 |
| 元件 | Component Diagram | 軟體元件間關係 | 分析、設計、實作 |
| 合成結構 | Composite Structure Diagram | 說明類別的內部結構，即內別中故部分之關係 | 分析、設計 |


#### 行為圖 (Behavior Diagrams)
> 系統之實體或物件間的動態關係

##### 互動行為(之間)

| 圖稱(中文) | 英文 | 用途 | 主要階段 | 備註 |
| ---- | --- | ---| ---|---|
| 循序 | Sequence Diagram | 活動的時序 | 分析、設計 |
| 溝通 | Communication Diagram | 活動的合作物件之間的溝通 | 分析、設計 |
| 互動概觀 | Interaction Overview Diagram | 程序的控制流程 | 分析、設計 |
| 時序 | Timing Diagram | 物件間所發生的互動以及其沿著時間軸所經歷的狀態改變 | 分析、設計 |


##### 作業行為(之內)

| 圖稱(中文) | 英文 | 用途 | 主要階段 | 備註 |
| ---- | --- | ---| ---|---|
| 活動 | Activity Diagram | 說明企業流程(無關乎類別)、使用案例中的活動流程，或方法的細節設計 | 分析、設計 |
| 行為狀態機 | Behavioral State Machines Diagram | 檢視類別行為，使用狀態、事件和轉換來描述單一物件的行為 | 分析、設計 | `行為狀態機` 可與 `協定狀態機` 合併 |
| 協定狀態機 | Protocol State Machines Diagram | 說明類別不同介面間的依存關係，協定狀態機不包含任何行為實作的內容，而只是描述事件和回應狀態的合法順序 | 分析、設計 |`行為狀態機` 可與 `協定狀態機` 合併|
|使用案例 | Use Case Diagram | 捕捉系統的企業需求，並說明系統與環境之間的互動關係 | 分析 |

