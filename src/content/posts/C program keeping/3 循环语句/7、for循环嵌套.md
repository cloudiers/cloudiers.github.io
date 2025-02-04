### 7.1、怎样用？

为了完成一些较为复杂的程序，在开发的时候，需要使用for循环的嵌套，其用法请看下图

![[_attachments/Pasted image 20250114142749.png]]

### 7.2、示例

> 打印1个直角三角形，用\*

![image-20230604173350164](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230604173350164.png)

> 注意
>
> - 每一行的列数和行号相对应，比如第 1 行就有 1 列，第 2 行有 2 列

参考代码如下

```c
//
// Created by wangmingdong on 2023/6/4.
//

#include "stdio.h"

int main() {

    for (int i = 1; i <= 5; i++) {  // 控制外层循环，主要用来换行
        for (int j=1; j<=i; j++) {  // 控制内层循环，主要用来在1行中打印多个*
            printf("* ");
        }
        printf("\n");
    }

    return 0;
}
```
