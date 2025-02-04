## [1. 是什么？](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/14.3.cmake?id=_1-%e6%98%af%e4%bb%80%e4%b9%88%ef%bc%9f)

一种可以生成编译规则文件的工具，例如它可以生成Makefile，这样就为开发人员节省了时间，提高了效率

## [2. cmake 与 Makefile的关系](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/14.3.cmake?id=_2-cmake-%e4%b8%8e-makefile%e7%9a%84%e5%85%b3%e7%b3%bb)

1. `CMake`可以生成`Makefile`：`CMake`根据`CMakeLists.txt`文件的描述，可以自动生成`Makefile`作为项目的构建脚本。这样，开发人员无需手动编写`Makefile`，而是使用`CMake`来生成适应不同编译器和平台的`Makefile`。
2. `CMake`提供更高级的功能：相比于手动编写`Makefile`，`CMake`提供了更高级的功能和灵活性。`CMake`可以处理跨平台问题，并支持多种编译器和构建系统。它可以自动生成适应不同环境的构建脚本，并提供更简洁和可读性强的配置语言。
3. `Makefile`更接近底层：`Makefile`是一种传统的构建脚本，更接近底层的构建系统。它提供了细粒度的控制和灵活性，适用于更复杂的构建场景和自定义需求。在某些情况下，开发人员可能需要手动编写和维护`Makefile`来满足特定的构建需求。

总的来说，`CMake`和`Makefile`是构建和管理项目的工具，它们之间有一定的关系。`CMake`可以生成`Makefile`作为构建脚本，但`CMake`提供了更高级和跨平台的功能，使得项目的构建更加方便和可扩展。使用`CMake`可以简化项目的构建过程，尤其在跨平台和多编译器的情况下

## [3. 示例](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/14.3.cmake?id=_3-%e7%a4%ba%e4%be%8b)

```c
cmake_minimum_required(VERSION 3.25)
project(Test2 C)

set(CMAKE_C_STANDARD 23)

add_executable(Test2 main.c)
```

执行如下命令：

```c
cmake -S . -B build -G "MinGW Makefiles"
```

- `-S .` ：表示源文件在当前目录
- `-B build`：表示生成的Makefile等文件存放的到build文件夹中
- `-G "这里是不同的Makefile规范"`：选择要用哪种Makefile

运行之后会看到一个`build`文件夹

![[_attachments/Pasted image 20250114145355.png]]

在`build`文件夹中，能够看到自动生成的`Makefile`文件

![[_attachments/Pasted image 20250114145400.png]]

然后进入到build文件夹，就可以使用make工具根据自动生成的Makefile文件中的内容进行编译项目，编译之后会生成可执行程序

![[_attachments/Pasted image 20250114145408.png]]
