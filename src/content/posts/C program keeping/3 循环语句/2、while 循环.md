### 2.1、基本格式

一般格式:

![[_attachments/Pasted image 20250114142550.png]]

说明：

- `控制条件`: 表达式A
- `循环体`: 语句

### 2.2、执行过程

![[_attachments/Pasted image 20250114142555.png]]

> 如果表达式A为 `真` 则 执行语句块1 , 执行完语句块1，之后 再次判断表达式A，如果为`真`则继续 执行语句块1，执行完语句块 1 之后再次判断表达式A
>
> 如此反复，直到表达式A的结果变为`假`，则跳出循环，也就意味着while循环语句执行结束

### 2.3、示例

> 要求：打印"i love c programming language" 8 次

参考代码如下：

```c
//
// Created by wangmingdong on 2023/6/4.
//

#include "stdio.h"

int main() {
    // 1. 定义一个变量，用来存储循环的次数
    int i = 1;

    // 2. 使用while循环实现重复执行代码
    while (i <= 8) {
        printf("i love c programming language\n");
        i++;
    }

    return 0;
}
```
