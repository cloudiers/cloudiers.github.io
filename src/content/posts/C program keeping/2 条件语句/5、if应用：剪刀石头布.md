### 5.1、运行效果

![[_attachments/Pasted image 20250114142326.png]]

### 5.2、补充知识：生成随机数

```c
//
// Created by wangmingdong on 2023/6/3.
//

#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int main() {

    srand((unsigned int) time(NULL));
    int ret1 = rand() % 10 + 1;  // 生成1~10的随机数
    int ret2 = rand() % 100 + 1;  // 生成1~100的随机数
    int ret3 = rand() % 34 + 66;  // 生成66~99的随机数
    printf("ret1=%d, ret2=%d, ret3=%d\n", ret1, ret2, ret3);

    // 总结的公式
    // int ret4 = rand() % (n - m + 1) + m;  // 生成m~n的随机数

    return 0;
}
```

### 5.3、剪刀石头布代码

```c
//
// Created by wangmingdong on 2023/6/3.
//

#include<stdio.h>
#include<stdlib.h>
#include<time.h>

int main() {

    // 1. 让程序生成一个随机数，用来充当电脑
    srand((unsigned int) time(NULL));
    int rand_num = rand() % 3 + 1;  // 生成1、2、3中的随机数，1表示剪刀  2石头  3布

    // 2. 从键盘获取一个数字，用来充当玩家
    printf("请输入(1剪刀 2石头 3布):");
    int player_num = -1;
    scanf("%d", &player_num);

    // 3. 对玩家的数据进行判断范围，是否在1、2、3之间
    if (player_num == 1 || player_num == 2 || player_num == 3) {

        // 提示用户系统当前正在进行处理中
        printf("系统正在判断输赢\n");
        printf("电脑:%d\n", rand_num);
        printf("玩家:%d\n", player_num);

        // 对输赢进行判断
        if ((player_num == 1 && rand_num == 3)  || (player_num == 2 && rand_num == 1) || (player_num == 3 && rand_num == 2)) {
            printf("玩家获胜...666\n");
        } else if (player_num == rand_num) {
            printf("平局...\n");
        } else {
            printf("输了...┭┮﹏┭┮\n");
        }
    } else {
        // 提示玩家，输入数据有误
        printf("您输入的数据有误，重新运行软件后请输入1、2、3之间的数字\n");
    }

    printf("别走啊，决战到天亮啊...算了这么晚了，明晚别忘了啊...\n");

    return 0;
}
```
