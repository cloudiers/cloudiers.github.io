## [1. 对于局部变量的修饰](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.7.static.extern?id=_1-%e5%af%b9%e4%ba%8e%e5%b1%80%e9%83%a8%e5%8f%98%e9%87%8f%e7%9a%84%e4%bf%ae%e9%a5%b0)

### [1.1 `static`的作用](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.7.static.extern?id=_11-static%e7%9a%84%e4%bd%9c%e7%94%a8)

1）延长局部变量的生命周期，从程序启动到程序退出，但是它并没有改变变量的作用域

2）定义变量的代码在整个程序运行期间仅仅会执行一次（当然可以通过指针再次访问这个变量）

示例（未添加`static`）

![image-20230612174022201](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230612174022201.png)

示例（添加`static`）

![image-20230612174052385](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/assets/image-20230612174052385.png)

说明：

- 第一次调用`add`函数时，`a`的值为初始值为`10`，然后`a++` 变为`11`；
- 以后 再调用`add`函数时，变量`a`会保存上一次调用后的结果，所以此时`a`的 值为`11`，然后`a++`变为`12`

总结一句话：

- 如果局部变量前有`static`修饰，那么这个变量会保存上一次调用此函数后的结果

### [1.2 `extern`的作用](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.7.static.extern?id=_12-extern%e7%9a%84%e4%bd%9c%e7%94%a8)

`extern`不是定义局部变量，它用在函数内部是声明一个全局变量

很少用`extern`修饰一个局部变量，没有太多实际意义，它一般用来声明全局变量

## [2. 对全局变量的修饰](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.7.static.extern?id=_2-%e5%af%b9%e5%85%a8%e5%b1%80%e5%8f%98%e9%87%8f%e7%9a%84%e4%bf%ae%e9%a5%b0)

### [2.1 `static`的作用](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.7.static.extern?id=_21-static%e7%9a%84%e4%bd%9c%e7%94%a8)

用`static`修饰的全局变量，会导致作用域局限于一个源文件内，只能为该源文件内的函数用，因此可以避免在其它源文件中引起错误

### [2.2 `extern`的作用](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.7.static.extern?id=_22-extern%e7%9a%84%e4%bd%9c%e7%94%a8)

用`extern`声明的全局变量，就是一个其它文件中的全局变量，这种方式常用

## [3. 对函数的修饰](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.7.static.extern?id=_3-%e5%af%b9%e5%87%bd%e6%95%b0%e7%9a%84%e4%bf%ae%e9%a5%b0)

内部函数：只能被本源文件中其他函数所调用，成为内部函数，用 `static`修饰

外部函数：能被其它源文件访问，用`extern`修饰，默认情况就是 `extern`
