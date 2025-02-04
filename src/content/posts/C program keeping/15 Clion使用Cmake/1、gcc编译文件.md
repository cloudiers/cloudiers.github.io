## [0. 注意](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/14.1.gcc?id=_0-%e6%b3%a8%e6%84%8f)

需要提前配置，系统环境的PATH，如下图

![[_attachments/Pasted image 20250114145154.png]]

将上图中的红框标记中的路径修改为自己Clion安装的路径即可

## [1. 编译过程](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/14.1.gcc?id=_1-%e7%bc%96%e8%af%91%e8%bf%87%e7%a8%8b)

有4步骤

1. 预编译
2. 编译
3. 汇编
4. 连接

## [2. 手动编译单文件](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/14.1.gcc?id=_2-%e6%89%8b%e5%8a%a8%e7%bc%96%e8%af%91%e5%8d%95%e6%96%87%e4%bb%b6)

假如有`test.c`，代码如下：

```c
//
// Created by wangmingdong on 2023/6/13.
//
#include <stdio.h>

int main() {
    printf("大家好，我是王铭东老师，网站 www.itprojects.cn");
    return 0;
}
```

1）打开终端

![[_attachments/Pasted image 20250114145201.png]]

2）查看是否可以使用gcc命令

![[_attachments/Pasted image 20250114145209.png]]

3）预编译

![[_attachments/Pasted image 20250114145214.png]]

![[_attachments/Pasted image 20250114145219.png]]

可以看到`test.i`文件，就是预编译之后的文件，实现了`#include`的替换操作

![[_attachments/Pasted image 20250114145228.png]]

4）编译

![[_attachments/Pasted image 20250114145234.png]]

5）汇编

![[_attachments/Pasted image 20250114145239.png]]

6）连接

![[_attachments/Pasted image 20250114145244.png]]

7）执行

![[_attachments/Pasted image 20250114145251.png]]

## [3. 预编译注意点](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/14.1.gcc?id=_3-%e9%a2%84%e7%bc%96%e8%af%91%e6%b3%a8%e6%84%8f%e7%82%b9)

![[_attachments/Pasted image 20250114145259.png]]

将`#define`定义的数据进行替换，执行`#if`等操作

![[_attachments/Pasted image 20250114145305.png]]
