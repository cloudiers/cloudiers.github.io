### 6.1、语法格式

![[_attachments/Pasted image 20250114142731.png]]

### 6.2、执行过程

![[_attachments/Pasted image 20250114142735.png]]

1. ①执行1次`表达式1`
2. ②判断`表达式2`的结果是否为`真`（就是结果是否是非0）

   1. 如果不是非0（就是说`表达式2`结果为`假`），直接结束整个for循环
   2. 如果是非0（就是`表达式2`结果为`真`）

      1. 那么就执行`{ }`中的代码（这些代码其实就是要重复执行的代码）
      2. 然后执行`表达式3`

      接下来从上述②标记的位置重复执行，直到`表达式2`的语句的结果为假的时候结束这个`for`循环

### 6.3、示例

> 要求：打印"i love c programming language" 8 次

代码如下

```c
//
// Created by wangmingdong on 2023/6/4.
//

#include "stdio.h"

int main() {

    for (int i = 1; i <= 8; i++) {
        printf("i love c programming language\n");
    }

    return 0;
}
```

### 6.4、练习

> 计算 1 到 100 的和

```c
//
// Created by wangmingdong on 2023/6/4.
//

#include "stdio.h"

int main() {

    int sum_result = 0;
    for (int i = 1; i <= 100; i++) {
        sum_result += i;
    }

    printf("1...100的累加和:%d\n", sum_result);

    return 0;
}
```

> 输出1~20之间的偶数

```c
//
// Created by wangmingdong on 2023/6/4.
//

#include "stdio.h"

int main() {

    for (int i = 1; i <= 20; i++) {
        if (i % 2 == 0) {
            printf("%d ", i);
        }
    }

    return 0;
}
```
