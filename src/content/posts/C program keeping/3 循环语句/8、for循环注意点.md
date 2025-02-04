### 8.1、死循环（无限循环）

表达式省略(三个表达式都可以省略)

![[_attachments/Pasted image 20250114142834.png]]

### 8.2、可以有多个表达式

![[_attachments/Pasted image 20250114142839.png]]

`表达式1`、`表达式2`、`表达式3`可以是一个简单的表达式，也可以是`逗号表达式`

```c
//
// Created by wangmingdong on 2023/6/4.
//

#include "stdio.h"

int main() {

    for (int i = 1, j = 1; i <= 2, j <= 3; i++, j++) {
        printf("i=%d, j=%d\n", i, j);
    }

    return 0;
}
```

运行效果

![[_attachments/Pasted image 20250114142848.png]]
