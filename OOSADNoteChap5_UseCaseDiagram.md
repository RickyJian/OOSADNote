# Unit 5 使用案例圖 (Use Case Diagram)
> **功能性圖**，描繪出系統的基本功能

![UseCaseDiagram](/images/UseCaseDiagram.PNG "UseCaseDiagram") 

* 主題(系統)邊界 (subject / system boundary)
    > 決定系統功能範圍 定義何人(`參與者`)使用此系統，以及系統提供什麼服務 (`使用案例`)
    > 名稱放在最上方 

* 參與者 ( actor / role ) 
    > 定義外部系統實體直接與系統互動扮演的角色
    > 使用系統的人或事 <br>
    > 提供輸入接受輸出 <br>
    > 放在`主題邊界`之外 

* 關係 (Relationship)

    * 關聯 (association)
        > `使用案例`與`參與者`之間的溝通

    * 延伸 (extend) 
        > 延伸功能，不必然發生

    * 含括 (include)
        > 使用案例功能，包含在另一個使用案例內，必然發生 <br>
        > 功能分解 (functional decomposition)  

    * 一般化 (generalization) 
        > 繼承特性

* 使用案例 ( use case)
    > 系統功能 <br>
    > 可`延伸`和`含括` <br>
    > 放置於`系統邊界`內  <br>
    > 由`參與者`執行 ， 以`參與者`角度撰寫



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