# 關係 (OOSADNote_Relationship)

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

### Aggregation

### Composition

### 關聯語法

* 關聯名稱：動詞片語，指明來源動作要求另外一個物件進行何種動作
* 角色名稱：物件所扮演的角色名詞
* 多重性(Multiplicity)：限制條件
* 可通性(Navigability)：表示訊息可以從來源類別的物件中轉移至目標類別一個以上的物件，而物件數量取決於多重性的值，「訊息傳送的方向」

## 相依 (Dependency)

當一個關聯中的元件改變時，會有想到其他元件

![Dependency](/images/Relationship_Dependency.PNG "Dependency") 