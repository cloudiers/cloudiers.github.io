## [1. 是什么？](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.2.typedef?id=_1-%e6%98%af%e4%bb%80%e4%b9%88%ef%bc%9f)

C语言不仅供了丰富的数据类型，而且还允许由用户自己定义类型说明符，也就是说允许用户为数据类型取“别名”(起外号)

作用是简化代码，减少声明错误

定义的格式：

![[_attachments/Pasted image 20250114144012.png]]

## [2. 技巧](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.2.typedef?id=_2-%e6%8a%80%e5%b7%a7)

给一个已经存在的类型取别名是有技巧的，简单来说，分为3步

1）用原类型定义一个变量，比如，想为`unsigned char`取别名

```
unsigned char A;
```

2）把变量名替换为“别名”

```
unsigned char uchar;
```

3）在最前面添加typedef

```
typedef unsigned char uchar;
```

## [3. 使用方法](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.2.typedef?id=_3-%e4%bd%bf%e7%94%a8%e6%96%b9%e6%b3%95)

### [1）基本数据类型](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.2.typedef?id=_1%ef%bc%89%e5%9f%ba%e6%9c%ac%e6%95%b0%e6%8d%ae%e7%b1%bb%e5%9e%8b)

例如,有整型变量`a`、b，其说明如下:

```
int a,b;
```

其中

- `int`是整型变量的类型说明符
- `int`的完整写法为`integer`，为了增加程序的可读性，可把整型说明符用`typedef`定义为:

```
typedef int INTEGER;
```

这以后就可用`INTEGER`来代替`int`作整型变量的类型说明了

例如:

```
INTEGER a,b; //它等效于: int a,b;
```

用`typedef`定义数组、指针、结构等类型将带来很大的方便，不仅使程序书写简单而且使意义更为明确，因而增强了可读性

### [2）数组类型](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.2.typedef?id=_2%ef%bc%89%e6%95%b0%e7%bb%84%e7%b1%bb%e5%9e%8b)

如:

```
typedef char NAME[20];
```

表示

- `NAME`是字符数组类型，数组长度为20
- 然后可用NAME 定义变量，如:

```
NAME a1,a2,s1,s2;
```

完全等效于

```
char a1[20], a2[20], s1[20], s2[20];
```

### [3）结构体类型](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.2.typedef?id=_3%ef%bc%89%e7%bb%93%e6%9e%84%e4%bd%93%e7%b1%bb%e5%9e%8b)

第1种

```
typedef struct Person{
    int age;
    char *name;
} PersonType;
```

第2种

```
typedef struct{
    int year;
    int month;
    int day;
} Date;
```

第3种

```
typedef struct Person PersonType;
```

### [4）枚举类型](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.2.typedef?id=_4%ef%bc%89%e6%9e%9a%e4%b8%be%e7%b1%bb%e5%9e%8b)

第1种

```
enum Sex{ SexMan, SexWoman, SexOther };
typedef enum Sex SexType;
```

第2种

```
typedef enum _Sex{ SexMan, SexWoman, SexOther } Sex;
Sex sex = SexOther;
```

第3种

```
typedef enum{ ColorRed, ColorBule, ColorGreen, ColorYellow} Color;
Color color = ColorGreen;
```

### [5）函数指针](https://doc.itprojects.cn/0004.zhishi.c/0002.doc/index.html#/10.2.typedef?id=_5%ef%bc%89%e5%87%bd%e6%95%b0%e6%8c%87%e9%92%88)

```
// 给指针函数起别名
typedef int (*FUN)(int, int);
// 用别名定义两个指针变量
FUN f1,f2;
// 给函数指针初始化
f1 = sum;  // sum是1个函数的名字
printf("%d\n",f1(12,34));
```

注意：

- 有时也可用宏定义来代替`typedef`的功能，但是宏定义是由预处理完成的，而`typedef`则是在编译时完成的，后者更为灵活方便
