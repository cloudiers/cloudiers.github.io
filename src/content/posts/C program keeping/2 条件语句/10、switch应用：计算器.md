### 10.1、运行效果

![[_attachments/Pasted image 20250114142508.png]]

### 10.2、代码

```c
//
// Created by wangmingdong on 2023/6/3.
//

#include<stdio.h>

int main() {

    int num1, num2;

    printf("请输入第1个数:");
    scanf("%d", &num1);

    printf("请输入第2个数:");
    scanf("%d", &num2);

    printf("输入您的选择(+-*/):");
    char option;
    scanf("%c", &option);  // 这个多1次scanf的作用是将上一次输入的 换行符号 获取；如果只有一次%c的话 会将换行符赋值给option变量
    scanf("%c", &option);

    switch (option) {
        case '+':
            printf("%d %c %d = %d\n", num1, option, num2, num1 + num2);
            break;
        case '-':
            printf("%d %c %d = %d\n", num1, option, num2, num1 - num2);
            break;
        case '*':
            printf("%d %c %d = %d\n", num1, option, num2, num1 * num2);
            break;
        case '/':
            printf("%d %c %d = %d\n", num1, option, num2, num1 / num2);
            break;
        default:
            printf("输入有误....");
    }

    return 0;
}
```
