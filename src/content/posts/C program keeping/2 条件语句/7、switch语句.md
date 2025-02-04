### 7.1、有什么用？

可以对一个结果进行多次判断，有时候比if的写法简洁很多

### 7.2、使用格式

![[_attachments/Pasted image 20250114142415.png]]

执行顺序 :

1. 计算表达式A的值
2. 接下来把这个值，顺序与常量表达式1,2..n的值进行比较；当第一次 遇到相等时，则执行冒号与break之间的语句
3. 当冒号与break之间的语句执行完毕后，就代表这个switch执行结束

若表达式A的值与所有常量表达式的值都不相等，则执行 default对应的语句n+1，然后结束switch语句

### 7.3、示例

```c
//
// Created by wangmingdong on 2023/6/3.
//

#include<stdio.h>

int main() {
    int day = 0;

    printf("请输入一个数字(1~7):");
    scanf("%d", &day);

    switch (day) {
        case 1: printf("星期1");break;
        case 2: printf("星期2");break;
        case 3: printf("星期3");break;
        case 4: printf("星期4");break;
        case 5: printf("星期5");break;
        case 6: printf("星期6");break;
        case 7: printf("星期7");break;
        default: printf("输入有误...");
    }

    return 0;
}
```

如果不用上面的switch，用if的话，你会怎么写呢？请自己编写，然后与switch进行对比，你就知道switch的好处了

### 7.4、想一想

看下图，你悟道什么吗？

![[_attachments/Pasted image 20250114142422.png]]
