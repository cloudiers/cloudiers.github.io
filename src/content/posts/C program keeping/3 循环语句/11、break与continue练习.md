## [1. `break`练习](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/3.11.break.continue.lianxi?id=_1-break%e7%bb%83%e4%b9%a0)

编写代码，试下如下要求

> 计算半径r从1~10的圆面积，并且面积area不能大于100，输出 r 和对应的 area

思考:

> r 从 1 变到 10 判断面积是否不是>100 如果大于>100 循环要终止 面积 = `3.14 * r * r`;

```c
//
// Created by wangmingdong on 2023/6/4.
//

#include "stdio.h"

int main() {
    float area = 0;
    for (int r = 1; r <= 10; r++) {
        area = r * r * 3.14;
        if (area > 100) {
            break;
        }
        printf("r=%d, area=%f\n", r, area);
    }

    return 0;
}
```

## [2. `continue`练习](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/3.11.break.continue.lianxi?id=_2-continue%e7%bb%83%e4%b9%a0)

编写代码，试下如下要求

> 输出1~100之间的不能被3整除的数

```c
//
// Created by wangmingdong on 2023/6/4.
//

#include "stdio.h"

int main() {

    for (int i = 1; i <= 100; i++) {
        if (i % 3 == 0) {
            continue;
        }
        printf("i=%d\n", i);
    }

    return 0;
}
```
