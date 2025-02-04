### 2.1、if语句的作用

类似生活中，到了一个路口进行选择一样，程序中`if`语句就可以完成根据不同的结果执行不同的语句

![[_attachments/Pasted image 20250114142122.png]]

### 2.2、第1种格式

![[_attachments/Pasted image 20250114142130.png]]

> 如果表达式结果为真（就是条件满足），执行语句1，否则不执行语句1，而是直接跳过语句1，继续执行后续的语句代码

```c
//
// Created by wangmingdong on 2023/6/2.
//
#include "stdio.h"

int main() {
    int age = 35;

    printf("接下要系统要对您的年龄进行验证\n");

    if (age >= 18) {
        printf("您的年龄已满足18岁以上，可以学习机动车驾驶证了");
    }
    printf("欢迎再次光临哈，bye");

    return 0;
}
```

执行结果

![[_attachments/msedge_VAyACJHmT2.png]]

### 2.3、第 2 种格式

![[_attachments/Pasted image 20250114142156.png]]

> 如果表达式结果为真（就是条件满足），执行语句块1，否则不执行语句1，而是执行语句2，当语句2执行完后会继续执行后续的语句代码

```c
//
// Created by wangmingdong on 2023/6/2.
//
#include "stdio.h"

int main() {
    int age = 15;

    printf("接下要系统要对您的年龄进行验证\n");

    if (age >= 18) {
        printf("您的年龄已满足18岁以上，可以学习机动车驾驶证了");
    } else {
        printf("您的年龄不满足18岁以上，等您长大后再来吧，我等您...");
    }
    printf("欢迎再次光临哈，bye");

    return 0;
}
```

![[_attachments/Pasted image 20250114142208.png]]
