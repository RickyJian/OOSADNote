# Unit 6 類別圖 (Class Diagram)

對一組擁有相同屬性、動作、方法、關係與行為的物件的一段描述

![Class](/images/Class_TopGround.PNG "Class")
![Symbol](/images/Class_Symbol.PNG "Symbol") 


> 具體類別 (concrete class)：用來建立物件 <br>
> 抽象類別 (abstract class)：表達抽象概念

## 名稱區塊

* 駝峰字
* 名詞或動名詞

## 屬性區塊 (attribute)

格式：visibility name : type [multiplicity] = initialValue <br>

描述類別資訊

### 衍生屬性(derived attribute)

經由計算或推導所得的屬性，在屬性前面加斜線(`/`)

### 初值 (initial value)

物件建立時設定的直

## 動作區塊 (operation)

格式：visibility name (parameterName:parameterType ...) :returnType

<br>

類別中的功能

* 名稱
* 參數
* 回傳型別

## 可見性 (Visibility)

裝飾 | 名稱(中) | 名稱(英) | 語意
---------|----------|---------|---------
`+` | 公開 | Public | 任何元件都會存取
`-` | 隱藏 | Private | 類別中才能存取
`#` | 保護 | Protected | 類別、子類別能存取
`～` | 套件 | Package | 同一套件或子套件能存取


## 多重性 (Multiplicity)

說明關係上的數量

* 集合(Collection)：值大於1代表物件是集合
* 空值(Null)：表示物件本身尚未建立，例：[0..1]


![Multiplicity](/images/Class_Multiplicity.PNG "Multiplicity")

## 關係 (relationship)

### 一般化關係 (generalization)

繼承，`a-kind-of`代表

![Generaization](/images/Class_Generaization.PNG "Generaization") 

#### 超類別(superclass) 

父類別

#### 子類別(subclass)

會繼承`超類別`屬性及操作

> 可替代性原則(principle of substitutability)：若`子類別`屬性及操作與`超類別`一樣，則能取代


### 關聯關係 (association)

常用在類別

![Association](/images/Class_Association2.PNG "Association")

![Relationship](/images/Relationship.PNG "Relationship")  

#### 組合關係 (aggregation)

把部分(parts)關連到全部(whole)，或把部分關連到組合(assemble)。本質上基本是雙向。邏輯性。 <br>
比較弱的關係，兩物件的生命週期各自獨立，也就是說物件並不負責另一個的產生和刪除。

* `a-part-of`：邏輯的或實體的
* `a-member-of`：如集合成員關係
* `contained-in`
* `related-to`
* `associated-with`
* `has a`

![Aggregation](/images/Class_Aggregation.PNG "Aggregation") 

#### 組成關係 (Composition)

與組合關係相似，物理性，例：樹與葉子關係 <br>
比較強的關係，子關係依賴父關係，也就是說父物件刪除會影響子物件，同生共死

![Composition](/images/Class_Composition.PNG "Composition") 

`Owns a`

## 簡化類別圖

簡化複雜類別圖

### 觀點 (View)

1. 類別圖子集合
2. 顯示某個特定類型的關係
3. 限制類別所能顯示的資訊

### 使用套件 (Package)

將類別集合起來變成套件

## 物件與類別相依

類別實例化

![Instantiate](/images/ClassObject_Dependency.PNG "Instantiate")

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