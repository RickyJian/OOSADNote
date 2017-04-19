# Unit 5 使用案例圖 (Use Case Diagram)
> **功能性圖**，描繪出系統的基本功能
> 一連串的動作，包括變動的順序與錯誤的順序，使系統、子系統或是類別能與actor互動

![UseCaseDiagram](/images/UseCaseDiagram.PNG "UseCaseDiagram") 

* 主題(系統)邊界 (subject / system boundary)
    > 決定系統功能範圍 定義何人(`參與者`)使用此系統，以及系統提供什麼服務 (`使用案例`)
    > 名稱放在最上方 

* 參與者 ( actor / role ) 
    > 定義外部系統實體直接與系統互動扮演的角色
    > 使用系統的人或事 <br>
    > 提供輸入接受輸出 <br>
    > 放在`主題邊界`之外 

    1. 主要參與者
        > 實際啟用`使用案例`的參與者

    2. 次要參與者 
        > 啟用後，與`使用案例`互動的參與者

* 關係 (Relationship)

    * 關聯 (association)
        > `使用案例`與`參與者`之間的溝通

    * 延伸 (extend) 
        > 延伸功能，不必然發生 <br>
        > 現存的使用案例插入新的行為片段

        ![Extend](/images/UseCase_E.PNG "Extend")

    * 含括 (include)
        > 使用案例功能，包含在另一個使用案例內，必然發生 <br>
        > 功能分解 (functional decomposition)  

        1. 基本使用案例 (Base Use Case)
        2. 內含使用案例 (Inclusion Use Case)

            > 被包含的使用案例

        ![Include](/images/UseCase_I.PNG "Include")
        

    * 一般化 (generalization) 
        > 繼承特性

    1. `參與者`與`一般化`關係
        > 多個參與者在互動上有許多的共通點，可以將共同用到的功能建成一個`參與者`並`關聯`他

        * 未一般化 <br>
            ![NG](/images/UseCase_NG.PNG "NG")
        * 一般化 <br>
            ![NG](/images/UseCase_G.PNG "NG")
    
    2. `使用案例`與`一般化`關係
        > 子案例會比父案例更具體
        > * 繼承父使用案例特徵
        > * 加上新特徵
        > * 複寫繼承特徵

        ![UGL](/images/UseCase_UGL.PNG "UGL")

        ![UG](/images/UseCase_UG.PNG "UG")

* 使用案例 ( use case)
    > 系統功能 <br>
    > 可`延伸`和`含括` <br>
    > 放置於`系統邊界`內  <br>
    > 由`參與者`執行 ， 以`參與者`角度撰寫

### 使用案例規格(use case specification)
 ![UseCaseSpecification](/images/UseCase_UseCaseSpecification.PNG "UseCaseSpecification")

### 前置條件
> 系統啟動前必須達到的條件

### 後置條件
> `使用案例`完成後必須達到的條件

---
## 補充

| 名稱(中文) | 名稱(英文) | 用途 | 圖示 |
|---|---|---|---|
| 主題(系統)邊界 | subject/system boundary | 決定系統功能範圍 | ![subject](/images/UseCase_Subject.PNG "subject") |
| 參與者 | actor / role | 使用系統的人或事 | ![Actor](/images/UseCase_actor.PNG "Actor") |
| 使用案例 | use case | 使用系統的人或事 | ![Use Case](/images/UseCase_UseCase.PNG "Use Case") |
| 關聯 | association | `使用案例`與`參與者`之間的溝通 | ![Use Case](/images/UseCase_Association.PNG "Use Case") |
| 包括 | include | 使用案例功能，包含在另一個使用案例內 <br> 必然發生 | ![include](/images/UseCase_Include.PNG "include") |
| 延伸 | extend | 延伸功能，不必然發生 | ![extend](/images/UseCase_Extend.PNG "extend") |
| 一般化 | generalization | 繼承關係 | ![Generilization](/images/UseCase_Generilization.PNG "Generilization") |