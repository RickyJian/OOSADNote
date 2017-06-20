# 關係 (Relationship)

有意義的連接線

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
* 多重性(Multiplicity)：限制條件
* 可通性(Navigability)：表示訊息可以從來源類別的物件中轉移至目標類別一個以上的物件，而物件數量取決於多重性的值，「訊息傳送的方向」

![Association](/images/Relationship_Association.PNG "Association") 

## 相依 (Dependency)

當一個關聯中的元件改變時，會有想到其他元件

![Dependency](/images/Relationship_Dependency.PNG "Dependency") 