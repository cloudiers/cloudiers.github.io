### 10.1、什么是`break`

大白话：用来强制结束`整个循环`的关键字

### 10.2、什么是`continue`

大白话：用来强制结束本次循环的关键字

### 10.3、基本用法

想一想下面的程序会在终端中输出什么？

```c
#include "stdio.h"

int main() {

    for (int i = 1; i <= 3; i++) {
        printf("i=%d\n", i);
        if (i == 2) {
            // break;
            // continue;
        }
        printf("---------\n");
    }

    return 0;
}
```

#### 10.3.1、使用`break`

当`break`语句用于`do-while`、`while`、`for`循环语句中时，可使程序终止整个循环语句

![[_attachments/Pasted image 20250114142908.png]]

#### 10.3.2、使用`continue`

结束本次循环，继续下次循环

![[_attachments/Pasted image 20250114142918.png]]
