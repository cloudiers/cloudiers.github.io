### 11.1、运行效果

![[_attachments/Pasted image 20250114142516.png]]

### 11.2、代码

```c
//
// Created by wangmingdong on 2023/6/3.
//

#include<stdio.h>

int main() {

    int option_num = 0;

    printf("--------------------------------\n");
    printf("         人员管理系统 V1.0\n");
    printf("1: 添加人员信息\n");
    printf("2: 删除人员信息\n");
    printf("3: 修改人员信息\n");
    printf("4: 查询人员信息\n");
    printf("5: 显示所有人员信息\n");
    printf("6: 设置\n");
    printf("--------------------------------\n");

    printf("输入您的选择，然后按下回车>>>");
    scanf("%d", &option_num);

    switch (option_num) {
        case 1:
            printf("1: 添加人员信息\n");
            break;
        case 2:
            printf("2: 删除人员信息\n");
            break;
        case 3:
            printf("3: 修改人员信息\n");
            break;
        case 4:
            printf("4: 查询人员信息\n");
            break;
        case 5:
            printf("5: 显示所有人员信息\n");
            break;
        case 6:
            printf("6: 设置\n");
            printf(">>--------------------------------\n");
            printf("1: 添加密码\n");
            printf("2: 修改密码\n");
            printf("3: 删除密码\n");
            printf("0: 返回\n");
            printf("--------------------------------\n");

            printf("输入您的选择，然后按下回车>>>");
            scanf("%d", &option_num);

            switch (option_num) {
                case 1: printf("1: 添加密码\n"); break;
                case 2: printf("2: 修改密码\n"); break;
                case 3: printf("3: 删除密码\n"); break;
                case 0: printf("0: 返回\n"); break;
                default: printf("输入有误...");
            }

            break;
        default:
            printf("输入有误....");
    }

    return 0;
}
```
