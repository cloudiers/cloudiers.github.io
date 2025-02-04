### 6.1、if(条件) 可以直接写分号`;`表示什么也不干

> `;` 也是一个语句，名字叫做：空语句

```c
#include<stdio.h>

int main() {

    if (1==1);

    return 0;
}
```

### 6.2、布尔变量作条件

`if(1)`、`if(-1)` 或者其它的只要不是0，那么就表示`真`，即这个if判断语句结果成立

`if(0)` 表示`假`，即这个if判断语句结果不成立

```c
#include<stdio.h>

int main() {

    if (-1) {
        printf("我是测试1，你猜猜这行代码会执行吗?");
    }

    if (0) {
        printf("我是测试2，你猜猜这行代码会执行吗?");
    }

    return 0;
}
```

### 6.3、if语句的作用域（就是生效起作用的范围）问题

```c
#include<stdio.h>

int main() {
    int age = 35;

    if (age > 18) {
        printf("您的年龄大于18岁哦\n");
        int num = 1000;
    }
    printf("num = %d\n", num); // 这条语句会出现问题

    return 0;
}
```

上面的代码，`printf`中的`num`是不能用的，因为`num`是在`if`的大括号中进行定义的，即`num`的作用域为`if`后的左大括号到右大括号之间，所以`num`不能在`printf`中使用

![[_attachments/Pasted image 20250114142345.png]]

### ### 6.4、遇到省略大括号的if

```c
#include<stdio.h>

int main() {
    int age = 8;

    if (age >= 0)
    if (age < 5)
    printf("小儿\n");
    else if (age < 10)
    printf("小孩\n");
    if (age > 12)
    printf("小破孩\n");
    else
    printf("不知道\n");

    return 0;
}
```

> 上面的代码，估计有很多年编程经验的开发者也会很困惑的，因为没有大括号，所以导致这个程序的可续性非常差
>
> 建议在以后的学习或者开发中，尽量在if后加上大括号，除非你想被你老大或者同事鄙视!

幸好借助Clion这种高端的IDE集成开发环境软件，可以通过快捷键`alt+ctl+字母L`进行格式化，从而能够看懂

![[_attachments/Pasted image 20250114142408.png]]
