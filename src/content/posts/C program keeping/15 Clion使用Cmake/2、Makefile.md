## [1. 是什么？](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/14.2.makefile?id=_1-%e6%98%af%e4%bb%80%e4%b9%88%ef%bc%9f)

用来规定编译程序流程的文件

## [2. 示例](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/14.2.makefile?id=_2-%e7%a4%ba%e4%be%8b)

在《人员管理系统》-数据备份到文件 项目的文件夹中，新建文件`Makefile`，代码如下：

```c
main: main.o file.o link.o menu.o
    gcc main.o file.o link.o menu.o -o main

main.o:main.c
    gcc -E main.c -o main.i
    gcc -S main.i -o main.s
    gcc -c main.s -o main.o

link.o:link.c
    gcc -E link.c -o link.i
    gcc -S link.i -o link.s
    gcc -c link.s -o link.o

file.o:file.c
    gcc -E file.c -o file.i
    gcc -S file.i -o file.s
    gcc -c file.s -o file.o

menu.o:menu.c
    gcc -E menu.c -o menu.i
    gcc -S menu.i -o menu.s
    gcc -c menu.s -o menu.o
```

然后在终端中执行，如下命令

![[_attachments/Pasted image 20250114145326.png]]

最终在左侧目录栏能看到`main.exe`这个可以执行的程序

![[_attachments/Pasted image 20250114145338.png]]

## [3. 有什么用？](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/14.2.makefile?id=_3-%e6%9c%89%e4%bb%80%e4%b9%88%e7%94%a8%ef%bc%9f)

下面是Makefile的几个主要用途：

1. 自动化编译：Makefile定义了源代码文件之间的依赖关系和编译规则，可以自动检测源文件的变化并只编译发生改变的文件，以提高编译效率
2. 管理复杂项目：对于大型项目而言，通常有多个源文件和库文件需要编译和链接。Makefile可以管理这些文件之间的依赖关系，确保在需要重新编译时按照正确的顺序执行编译和链接操作
3. 跨平台支持：Makefile可以根据不同的操作系统和编译器来定义适应性强的构建规则，从而实现跨平台的代码编译和构建
4. 快速重建项目：Makefile可以定义清理目标，使得可以轻松地清除生成的目标文件、可执行文件和其他构建产物，以便重新开始构建项目

总之，Makefile是一个强大的工具，可以帮助开发人员管理和构建C语言项目，提高开发效率并确保正确构建代码
