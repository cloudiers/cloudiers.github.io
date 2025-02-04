### 4.1、使用格式

if语句的高级用法的格式如下

![[_attachments/Pasted image 20250114142308.png]]

- 说明
- 如果`表达式1`为真（就是条件满足），则执行`语句1`
- 否则判断`表达式2`，如果结果为真（就是条件满足），则执行`语句2`
- 否则判断`表达式3`，如果结果为真（就是条件满足），则执行`语句3`
- 当`表达式1、2、3`都不满足，会执行最后一个`else`语句

### 4.2、练习

请编写代码，实现如下要求

> 输入一个 0 ~ 100 之间的成绩，按0 - 59(E)， 60 - 69(D)， 70 - 79(C)， 80 - 89(B)， 90 - 100(A) 分成几等，分别输出对应的大写字母；
>
> 比如 用户输入的是 71 ，那么就输出C

```c
//
// Created by wangmingdong on 2023/6/2.
//
#include "stdio.h"

int main() {
    int score = 0;  // 用来存储分数

    // 1. 提示用户输入分数
    printf("请输入分数:");

    // 2. 获取分数
    scanf("%d", &score);

    // 3. 使用if进行判断
    if (score <= 100 && score >= 90) {
        printf("A");
    } else if (score <= 89 && score >= 80) {
        printf("B");
    } else if (score <= 79 && score >= 70) {
        printf("C");
    } else if (score <= 69 && score >= 60) {
        printf("D");
    } else if (score <= 59 && score >= 0) {
        printf("E");
    } else {
        printf("输入数据有误...");
    }

    return 0;
}
```

运行效果

![[_attachments/Pasted image 20250114142319.png]]
