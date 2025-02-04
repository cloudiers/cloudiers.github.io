## [1.](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/3.12.break.continue.zhuyidian?id=_1)

`break`和`continue`除了在`for`循环中使用，还可以在`while`、`do-while`循环，目的就是为了结束循环

## [2.](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/3.12.break.continue.zhuyidian?id=_2)

除了在循环中使用外不能单独出现`break`和`continue`（当然`break`可以在`switch`中用）

![[_attachments/Pasted image 20250114142932.png]]

## [3.](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/3.12.break.continue.zhuyidian?id=_3)

在嵌套的循环中，一个`break`语句只向外跳一层，即`break`和`continue`只在它们紧接着的外面的循环中有效

```c
//
// Created by wangmingdong on 2023/6/4.
//

#include "stdio.h"

int main() {


    for (int i = 1; i <= 3; i++) {
        printf("---------start--------%d\n", i);
        for (int j = 1; j <= 3; j++) {
            if (j == 2) {
                break;
            }
            printf("****\n");
        }
        printf("---------stop---------%d\n", i);
    }

    return 0;
}
```

运行效果

![[_attachments/Pasted image 20250114142941.png]]

总结

![[_attachments/Pasted image 20250114142948.png]]
