## [1. 目的](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/1.02.mingw?id=_1-%e7%9b%ae%e7%9a%84)

在学习`C语言`的期间，肯定需要创建很多个`.c`文件，每个`.c`文件都保存着自己编写的代码，例如`01.hello.c`里面是你好世界的源代码，`02.printf.c`里是一个输出数据的源码文件

如果想要在一个`C语言`工程中，创建多个`.c`文件，默认情况下`Clion`会自动帮我们用`CMake`进行管理

![image-20230601104139552](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104139552.png)

所谓的`CMake`就是一个编译多个.c文件为一个可执行程序（或者库）的工具

`CMake`功能很强，但是不适合当前我们新入门的同学（王老师会在本教程的末尾章节给大家讲解`CMake`，但是现在你不要用这它就对了）

怎么办？

答：`不用CMake，直接用MinGW编译`（可能这个你还不太清楚，没关系，后面慢慢就理解）

## [2. 不用CMake，怎样添加`.c`并进行编译运行呢？](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/1.02.mingw?id=_2-%e4%b8%8d%e7%94%a8cmake%ef%bc%8c%e6%80%8e%e6%a0%b7%e6%b7%bb%e5%8a%a0c%e5%b9%b6%e8%bf%9b%e8%a1%8c%e7%bc%96%e8%af%91%e8%bf%90%e8%a1%8c%e5%91%a2%ef%bc%9f)

![image-20230601104354433](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104354433.png)

![image-20230601104429568](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104429568.png)

![image-20230601104503424](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104503424.png)

![image-20230601104535685](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104535685.png)

![image-20230601104555828](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104555828.png)

![image-20230601104628414](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104628414.png)

![image-20230601104742760](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104742760.png)

![image-20230601104834691](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104834691.png)

![image-20230601104856665](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104856665.png)

![image-20230601104929800](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601104929800.png)

![image-20230601105009480](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601105009480.png)

### [注意：](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/1.02.mingw?id=%e6%b3%a8%e6%84%8f%ef%bc%9a)

- 上图的`main.exe`是一个可以在Windows上运行的程序了，也就意味着你可以在文件夹中找到这个文件，然后双击运行，但是.....这个程序不够完美，双击后一闪而过什么也看不到，不用紧张，这是正常现象,因为我们写的c语言代码就一个helloworld；如果想它给你一个漂亮的登录窗口，你需要继续学习才行。加油吧....

- 如果想要看到`main.exe`程序运行的结果，可以在终端中输入`main.exe`就可以运行了，见下图  
  ![image-20230601105403780](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601105403780.png) ![image-20230601105459496](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601105459496.png) ![image-20230601105544276](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601105544276.png) ![image-20230601105617664](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230601105617664.png)
