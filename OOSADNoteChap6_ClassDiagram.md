# Unit 6 類別圖 (Class Diagram)

對一組擁有相同屬性、動作、方法、關係與行為的物件的一段描述

![Object](/images/Class_TopGround.PNG "Object") 

> 具體類別 (concrete class)：用來建立物件 <br>
> 抽象類別 (abstract class)：表達抽象概念

## 屬性 (attribute)

描述類別資訊

### 衍生屬性(derived attribute)

經由計算或推導所得的屬性，在屬性前面加斜線(`/`)

## 操作 (operation)

行為

## 關係 (relationship)

### 一般化關係 (generalization)

繼承，`a-kind-of`代表

![Generaization](/images/Class_Generaization.PNG "Generaization") 

#### 超類別(superclass) 

父類別

#### 子類別(subclass)

會繼承`超類別`屬性及操作

> 可替代性原則(principle of substitutability)：若`子類別`屬性及操作與`超類別`一樣，則能取代

### 組合關係 (aggregation)

把部分(parts)關連到全部(whole)，或把部分關連到組合(assemble)。本質上基本是雙向。邏輯性

* `a-part-of`：邏輯的或實體的
* `a-member-of`：如集合成員關係
* `contained-in`
* `related-to`
* `associated-with`

![Aggregation](/images/Class_Aggregation.PNG "Aggregation") 

### 組成關係

與組合關係相似，物理性


![Composition](/images/Class_Composition.PNG "Composition") 


### 關聯關係 (association)

常用在類別

![Association](/images/Class_Association2.PNG "Association") 


## 可見性 (Visibility)

裝飾 | 名稱(中) | 名稱(英) | 語意
---------|----------|---------|---------
 `+` | 公開 | Public | 任何元件都會存取
 `-` | 隱藏 | Private | 類別中才能存取
 `#` | 保護 | Protected | 類別、子類別能存取
 `~` | 套件 | Package | 同一套件或子套件能存取

 -------

 # 補充

 ## CRC卡

 類別的責任與合作

 > C：Class <br>
 > R：Responsibilities <br>
 > C：Collaborators
  

 ### 責任 (responsibility)

 #### 知 (knowing)

哪些事情是類別實體能知道的

 #### 做 (doing)

 哪些事情是類別實體能做的