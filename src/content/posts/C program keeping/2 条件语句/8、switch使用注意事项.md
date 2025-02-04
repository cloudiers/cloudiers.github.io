### 8.1、`case`后面只能是`常量` 或者`常量表达式`，而且多个`case`后面的值不能出现相同的

![[_attachments/Pasted image 20250114142432.png]]

### 8.2、`default`可以省略吗?

答：可以省略，但是不建议，因为它的作用是对所有判断都不成立的时候 进行提示，这样给用户的体验更好

### 8.3、`default`一定要在最后吗?

答：不是，可以在任意位置。但是建议在最后。

![[_attachments/Pasted image 20250114142438.png]]

### 8.4、`break`可以省略吗?

答：最后一个可以省略，其他最好不要省略 ，会出现一个现象: `case穿透`

![[_attachments/Pasted image 20250114142445.png]]

但是也得分情况，有的时候，就可以不写break，见下代码

```c
//
// Created by wangmingdong on 2023/6/3.
//

#include<stdio.h>

int main() {
    int month = 0;

    printf("请输入一个农历月份(1~12):");
    scanf("%d", &month);

    switch (month) {
        case 3:
        case 4:
        case 5: printf("春季\n");break;
        case 6:
        case 7:
        case 8: printf("夏季\n");break;
        case 9:
        case 10:
        case 11: printf("秋季\n");break;
        case 12:
        case 1:
        case 2: printf("冬季\n");break;
        default: printf("输入有误...");
    }

    return 0;
}
```

### 8.5、`switch`语句表达式中，不能是`float`、`double`类型，因为它们俩是不精确的（`float`、`double`在底层实现的时候是用的近似值，所以不是精准值）

![[_attachments/Pasted image 20250114142454.png]]
