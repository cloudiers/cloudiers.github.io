### 15.1、`sizeof`运算符

获取操作数占用内存大小的字节数，使用方法如下:

![[_attachments/Pasted image 20250114141921.png]]

建议：选择方法1，带上括号，这也是绝大部分C语言编程人员的做法

### 15.2、使用方法

#### 15.2.1、sizeof使用形式

```c
sizeof(type)  // 数据类型必须用括号括住
```

```c
#include <stdio.h>

int main(int argc, char *argv[]) {
    int size = sizeof(int);
    printf("size=%d\n", size);
    size = sizeof(char);
    printf("size=%d\n", size);
    size = sizeof(short);
    printf("size=%d\n", size);
    size = sizeof(float);
    printf("size=%d\n", size);
    return 0;
}
```

![[_attachments/Pasted image 20250113102951.png]]

#### 15.2.2、用于常量

```c
#include <stdio.h>

int main(int argc, char *argv[]) {
    int size = sizeof(1);
    printf("size=%d\n", size);
    size = sizeof(1.1);  // 默认1.1是double类型
    printf("size=%d\n", size);
    size = sizeof(1.1f);  // 1.1f就是float类型
    printf("size=%d\n", size);
    size = sizeof('a');
    printf("size=%d\n", size);
    return 0;
}
```

![[_attachments/Pasted image 20250113103004.png]]

#### 15.2.3、用于变量

```c
#include <stdio.h>

int main(int argc, char *argv[]) {
    char a;
    int size;
    size = sizeof(a);
    printf("size=%d\n", size);
    size = sizeof a; // 省略了括号
    printf("size=%d\n", size);
    return 0;
}
```

![[_attachments/Pasted image 20250113103015.png]]

#### 15.2.4、注意

- 再次提醒使用sizeof时带上括号，这也是绝大部分C语言编程人员的做法
