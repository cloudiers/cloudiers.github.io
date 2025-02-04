### 3.1、格式

if语句的嵌套格式如下：

![[_attachments/Pasted image 20250114142251.png]]

### 3.2、示例

```c
//
// Created by wangmingdong on 2023/6/2.
//
#include "stdio.h"

int main() {
    int ticket = 1;  // 代表车票， 1 ：有， 0 ：没有
    int knife_length = 9;  // 代表刀的程度

    if (ticket == 1) {  // 有车票
        if (knife_length <= 10) {
            printf("可以上火车\n");
        } else {
            printf("不可以上火车，刀的长度超过规定的长度\n");
        }
    } else {
        printf("不可以上火车，请先去购买火车票\n");
    }

    return 0;
}
```

运行效果

![[_attachments/Pasted image 20250114142301.png]]
