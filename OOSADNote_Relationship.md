# 關係 (Relationship)

有意義的連接線<br>

四大關係

* Association
* Realization
* Dependency
* Generalization

<br>

* 參與者與使用案例間的關係(Association)
* 使用案例間的關係 (Generalization , `<<include>>` , `<<extend>>`)
* 參與者之間的關係 (Generalization)

## 鏈結 (Link)

物件間語意的連接

![Link](/images/Object_Link.PNG "Link") 

## 關聯 (Association)

類別間的關係

![Accociation](/images/Class_Association.PNG "Accociation") 

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

### 關聯語法

* 關聯名稱：動詞片語，指明來源動作要求另外一個物件進行何種動作
* 角色名稱：物件所扮演的角色名詞
* 多重性(Multiplicity)：定義參與物件數量之規則
* 限制條件
* 可通性(Navigability)：表示訊息可以從來源類別的物件中轉移至目標類別一個以上的物件，而物件數量取決於多重性的值，「訊息傳送的方向」

![Association](/images/Relationship_Association.PNG "Association") 

## 相依 (Dependency)

當一個關聯中的元件改變時，會影響到其他元件，發生於套件、物件或類別間

![Dependency](/images/Relationship_Dependency.PNG "Dependency") 

### 使用

使用者會使用供應者所提供的服務來執行其行為

#### << use >>

使用者在某方面能夠使用供應者所提供的服務

#### << call >>

使用者的動作能呼叫到供應者的動作

#### << parameter >>

提供者對於提供者是一種參數

#### << sesnd >>

使用者是一個動作，他會將供應者(一定是訊號)傳送到某格個目標去

#### << instantiate >>

使用者是供應者的實例

### 抽象

描述不同抽象程度物件的相依關係

#### << trace >>

供應者與使用者在不同模型上表現相同概念的關係

#### << substitude >>

執行時使用者可能會被供應者取代，方式是遵守約定與介面的基礎上

#### << refine >>

與`<< trace >>`相反，模型中類別可能會存在兩種版本

#### << derive >> 

表現出物體在某方面是從其他物體延伸而來的概念

### 許可

物體存取其他物體的能力

#### << access >>

發生在套件之間，一個套檢能夠存取另一個套件公開的內容

#### << import >>

與 `<< access >>` 相似，除了供應者的名稱領域會合併到使用者的名稱領域中，其他部分都一樣。

#### << permit >>

無視供應者的可視性(visibility)，使用者皆可存取到供應者的元件