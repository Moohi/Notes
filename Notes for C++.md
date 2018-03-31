## 一些问题

1. 引用与指针
2. 内存泄漏
3. 排序
4. 动态规划 递归(dijkstra)



## C和C++语言基础

参考书：《C++ primer》，《effective C++》，《STL源码解析》

- **extern，static，volatile，const，new与malloc区别**
- **C++多态性与虚函数**


- **指针和引用，指针与数组，智能指针**
- **类型转换：static_cast, dynamic_cast, const_cast, reinterpret_cast**
- **内联函数，宏定义**
- **内存管理，内存泄漏**
- **STL里set和map，红黑树**

## 数据结构与算法

### **Hash表**

- Hash表实现（拉链和分散地址）

- Hash策略常见的有哪些？

- STL中hash_map扩容发生什么？ 

  (1) 创建一个新桶，该桶是原来桶两倍大最接近的质数(判断n是不是质数的方法：用n除2到*sqrt*(*n*)范围内的数) ； 
  (2) 将原来桶里的数通过指针的转换，插入到新桶中(注意STL这里做的很精细，没有直接将数据从旧桶遍历拷贝数据插入到新桶，而是通过指针转换) 
  (3) 通过swap函数将新桶和旧桶交换，销毁新桶。

### **树**

- 二叉树结构，二叉查找树实现；
- 二叉树的六种遍历；
- 二叉树的按层遍历；
- 递归是解决二叉树相关问题的神级方法；
- 树的各种常见算法题([http://blog.csdn.net/xiajun07061225/article/details/12760493**](https://link.zhihu.com/?target=http%3A//blog.csdn.net/xiajun07061225/article/details/12760493))；
- **什么是红黑树？**
- **红黑树与AVL树的区别**
- **Trie树(字典树)**

### 图

最小生成树

单源最短路径 全局最短路径

### 链表**

- 链表和插入和删除，单向和双向链表都要会
- 链表的问题考虑多个指针和递归 
  (1) 反向打印链表(递归) 
  (2) 打印倒数第K个节点(前后指针) 
  (3) 链表是否有环(快慢指针)等等。

### **栈和队列**

- **队列和栈的区别**？(从实现，应用，自身特点多个方面来阐述，不要只说一个先入先出，先入后出，这个你会别人也会，要展现出你比别人掌握的更深)
- 典型的应用场景

### **海量数据问题**

- 十亿整数（随机生成，可重复）中前K最大的数 
- **十亿整数（随机生成，可重复）中出现频率最高的一千个**

### **排序算法**

- 排序算法，快排，建堆，和归并
- 每种算法的时间空间复杂度，最好最差平均情况

### **位运算**

### 布隆过滤器

几十亿个数经常要查找某一个数在不在里面，使用布隆过滤器，布隆过滤器的原理。布隆过滤器可能出现误判，怎么保证无误差？

## 网络与TCP/IP

参考书籍：《图解TCP/IP》，《TCP/IP详解 卷一》，《图解HTTP》，《HTTP权威指南》

- [TCP与UDP之间的区别](https://link.zhihu.com/?target=http%3A//blog.csdn.net/shanghairuoxiao/article/details/68927070) 
  (1) IP首部，TCP首部，UDP首部 
  (2) TCP和UDP区别 
  (3) TCP和UDP应用场景 
  (4) 如何实现可靠的UDP
- [TCP三次握手与四次挥手](https://link.zhihu.com/?target=http%3A//blog.csdn.net/shanghairuoxiao/article/details/68927100)
- [详细说明TCP状态迁移过程](https://link.zhihu.com/?target=http%3A//blog.csdn.net/shanghairuoxiao/article/details/68927100) 
  (1) 三次握手和四次挥手状态变化； 
  (2) 2MSL是什么状态？作用是什么？ 
  (3)三次握手为什么不是两次或者四次？
- [TCP相关技术](https://link.zhihu.com/?target=http%3A//blog.csdn.net/shanghairuoxiao/article/details/68927100)

1. TCP重发机制，Nagle算法
2. TCP的拥塞控制使用的算法和具体过程
3. TCP的窗口滑动

- [TCP客户与服务器模型，用到哪些函数](https://link.zhihu.com/?target=http%3A//blog.csdn.net/shanghairuoxiao/article/details/69803044)
- [UDP客户与服务器模型，用到哪些函数](https://link.zhihu.com/?target=http%3A//blog.csdn.net/shanghairuoxiao/article/details/69951345)
- [域名解析过程，ARP的机制，RARP的实现](https://link.zhihu.com/?target=http%3A//blog.csdn.net/shanghairuoxiao/article/details/68926923)
- Ping和TraceRoute实现原理

### HTTP

- **http/https 1.0、1.1、2.0的特点和区别**
- **get/post 区别**
- **HTTP返回状态码**
- **http 协议头相关**

http数据由请求行，首部字段，空行，报文主体四个部分组成 
首部字段分为：通用首部字段，请求首部字段，响应首部字段，实体首部字段

- **https与http的区别？如何实现加密传输？加解密方式？**
- **浏览器中输入一个URL发生什么，用到哪些协议？**

### **安全相关**

至少了解攻击的原理和基本的防御方法，常见的攻击方法有一下几种

- SQL注入
- XSS
- CSRF
- SYN洪水攻击
- APR欺骗

## 数据库

主要参考书籍：《数据库系统概念》，《高性能MySQL》

- SQL语言(内外连接，子查询，分组，聚集，嵌套，逻辑)
- MySQL索引方法？索引的优化？
- InnoDB与MyISAM区别？
- 事务的ACID
- 事务的四个隔离级别
- 查询优化(从索引上优化，从SQL语言上优化)
- B-与B+树区别？
- MySQL的联合索引(又称多列索引)是什么？生效的条件？
- 分库分表

## Linux

主要参考书籍：《现代操作系统》，《APUE》，《UNP》，《LINUX内核设计与实现》，《深入理解LINUX内核》

- **进程与线程**

(1) 进程与线程区别？ 
(2) 线程比进程具有哪些优势？ 
(3) 什么时候用多进程？什么时候用多线程？ 
(4) LINUX中进程和线程使用的几个函数？ 
(5) 线程同步？ 
在Windows下线程同步的方式有：互斥量，信号量，事件，关键代码段 
在Linux下线程同步的方式有：互斥锁，自旋锁，读写锁，屏障(并发完成同一项任务时，屏障的作用特别好使) 知道这些锁之间的区别，使用场景？

- **进程间通讯方式**

1. **匿名管道与命名管道的区别**：匿名管道只能在具有公共祖先的两个进程间使用。
2. **共享文件映射mmap** 
   mmap建立进程空间到文件的映射，在建立的时候并不直接将文件拷贝到物理内存，同样采用缺页终端。mmap映射一个具体的文件可以实现任意进程间共享内存，映射一个匿名文件，可以实现父子进程间共享内存。
3. **常见的信号有哪些？**：SIGINT，SIGKILL(不能被捕获)，SIGTERM(可以被捕获)，SIGSEGV，SIGCHLD，SIGALRM

- **内存管理**

1. 虚拟内存的作用？
2. 虚拟内存的实现？
3. 操作系统层面对内存的管理？
4. 内存池的作用？STL里[内存池如何实现**](https://link.zhihu.com/?target=https%3A//github.com/oscarwin/MemoryPool)？
5. 进程空间和内核空间对内存的管理不同？
6. Linux的slab层，VAM？
7. 伙伴算法
8. 高端内存

- **进程调度**

1. Linux进程分为两种，实时进程和非实时进程；
2. 优先级分为静态优先级和动态优先级，优先级的范围；
3. 调度策略
4. 交互进程通过平均睡眠时间而被奖励；

- **死锁**

(1) 死锁产生的条件； 
(2) 死锁的避免；

- **命令行**

1. Linux命令 在一个文件中，倒序打印第二行前100个大写字母

```
cat filename | head -n 2 | tail -n 1 | grep '[[:upper:]]' -o | tr -d '\n'| cut -c 1-100 | rev 

```

1. 与CPU，内存，磁盘相关的命令(top，free, df, fdisk)
2. 网络相关的命令netstat，tcpdump等
3. sed, awk, grep三个超强大的命名，分别用与格式化修改，统计，和正则查找
4. ipcs和ipcrm命令
5. 查找当前目录以及字母下以.c结尾的文件，且文件中包含”hello world”的文件的路径
6. 创建定时任务

- **IO模型**

1. **五种IO模型：**阻塞IO，非阻塞IO，IO复用，信号驱动式IO，异步IO
2. **select，poll，epoll的区别**

- 线程池，内存池 自己动手实现一遍

### Linux的API

- **fork与vfork区别** 
  fork和vfork都用于创建子进程。但是vfork创建子进程后，父进程阻塞，直到子进程调用exit()或者excle()。 
  对于内核中过程fork通过调用clone函数，然后clone函数调用do_fork()。do_fork()中调用copy_process()函数先复制task_struct结构体，然后复制其他关于内存，文件，寄存器等信息。fork采用写时拷贝技术，因此子进程和父进程的页表指向相同的页框。但是vfork不需要拷贝页表，因为父进程会一直阻塞，直接使用父进程页表。
- **exit()与_exit()区别** 
  exit()清理后进入内核，_exit()直接陷入内核。
- 孤儿进程与僵死进程

1. 孤儿进程是怎么产生的？
2. 僵死进程是怎么产生的？
3. 僵死进程的危害？
4. 如何避免僵死进程的产生？

- **Linux是如何避免内存碎片的**

1. 伙伴算法，用于管理物理内存，避免内存碎片;
2. 高速缓存Slab层用于管理内核分配内存，避免碎片。

- **共享内存的实现原理？** 
- 系统调用与库函数(open, close, create, lseek, write, read)
- 同步方法有哪些？

1. 互斥锁，自旋锁，信号量，读写锁，屏障
2. 互斥锁与自旋锁的区别：互斥锁得不到资源的时候阻塞，不占用cpu资源。自旋锁得不到资源的时候，不停的查询，而然占用cpu资源。
3. [死锁](https://link.zhihu.com/?target=http%3A//blog.csdn.net/shanghairuoxiao/article/details/70444940)

## 其他

- ++i是否是原子操作 
  明显不是，++i主要有三个步骤，把数据从内存放在寄存器上，在寄存器上进行自增，把数据从寄存器拷贝会内存，每个步骤都可能被中断。
- 判断大小端

### 设计模式

- [单例模式线程安全的写法](https://link.zhihu.com/?target=http%3A//www.jellythink.com/archives/82)
- STL里的迭代器模式，适配器模式

### 分布式系统

- [map_reduce原理](https://link.zhihu.com/?target=http%3A//blog.jobbole.com/80619/) （这篇文章讲的很通俗易懂）
- 负载均衡
- CDN

## 参考

[知乎：C++ 后台开发面试时一般考察什么？- Oscarwin的回答](https://www.zhihu.com/question/34574154/answer/253165162?utm_source=qq&utm_medium=social)



## extern关键字

###  基本解释：

extern可以置于变量或者函数前，以标示变量或者函数的定义在别的文件中，提示编译器遇到此变量和函数时在其他模块中寻找其定义。此外extern也可用来进行链接指定。

也就是说extern有两个作用：***第一个***,当它与"C"一起连用时，如: extern "C" void fun(int a, int b);则告诉编译器在编译fun这个函数名时按着C的规则去翻译相应的函数名而不是C++的，因为C++支持函数的重载，C++的规则在翻译这个函数名时会把fun这个名字变得面目全非，可能是fun@aBc_int_int#%$也可能是别的，在这里不过多的论述这个问题。  

***第二***，当extern不与"C"在一起修饰变量或函数时，如在头文件中: extern int g_Int; 它的作用就是声明函数或全局变量的作用范围的关键字，其声明的函数和变量可以在本模块或其他模块中使用。

### extern变量

在一个源文件里定义了一个数组：char a[6];在另外一个文件里用下列语句进行了声明：extern char *a；请问，这样可以吗？ 

答案与分析：

不可以，程序运行时会告诉你非法访问。原因在于，指向类型T的指针并不等价于类型T的数组。extern char \*a声明的是一个指针变量而不是字符数组，因此与实际的定义不同，从而造成运行时非法访问。应该将声明改为**extern char a[ ]**。*

如果a[] = "abcd",则外部变量a=0x61626364 (abcd的ASCII码值)，*a显然没有意义，显然a指向的空间（0x61626364）没有意义，易出现非法内存访问。

extern用在变量声明中常常有这样一个作用，你在*.c文件中声明了一个全局的变量，这个全局的变量如果要被引用，就放在*.h中并用extern来声明。

### 单方面修改extern 函数原型

当函数提供方单方面修改函数原型时，如果使用方不知情继续沿用原来的extern申明，这样编译时编译器不会报错。但是在运行过程中，因为少了或者多了输入参数，往往会照成系统错误，这种情况应该如何解决？

答案与分析：

目前业界针没有一个很完美的方案，通常的做法是提供方在自己的xxx_pub.h中提供对外部接口的声明，然后调用方include该头文件，从而省去extern这一步。以避免这种错误。

### extern “C”

在C++环境下使用C函数的时候，常常会出现编译器无法找到obj模块中的C函数定义，从而导致链接失败的情况，应该如何解决这种情况呢？

答案与分析：

C++语言在编译的时候为了解决函数的多态问题，会将函数名和参数联合起来生成一个中间的函数名称，而C语言则不会，因此会造成链接时找不到对应函数的情况，此时C函数就需要用extern “C”进行链接指定，这告诉编译器，请保持我的名称，不要给我生成用于链接的中间函数名。

下面是一个标准的写法：

```c++
//在.h文件的头上
#ifdef __cplusplus
#if __cplusplus
extern "C"{
#endif
#endif /* __cplusplus */ 

	…
	…

//.h文件结束的地方
#ifdef __cplusplus
#if __cplusplus
}
#endif
#endif /* __cplusplus */ 
```


### extern函数声明

常常见extern放在函数的前面成为函数声明的一部分，那么，C语言的关键字extern在函数的声明中起什么作用？

答案与分析：

如果函数的声明中带有关键字extern，仅仅是暗示这个函数可能在别的源文件里定义，没有其它作用。即下述两个函数声明没有明显的区别：
extern int f(); 和int f();

当然，这样的用处还是有的，就是在程序中取代include “*.h”来声明函数，在一些复杂的项目中，我比较习惯在所有的函数声明前添加extern修饰。关于这样做的原因和利弊可见下面的这个例子：“用extern修饰的全局变量”

```c++
//test1.h
#ifndef TEST1H
#define TEST1H
extern char g_str[]; // 声明全局变量g_str
void fun1();
#endif
```

```c++
//test1.cpp
#include "test1.h"
char g_str[] = "123456"; // 定义全局变量g_str
void fun1() { cout << g_str << endl; }
```


```c++
//test2.cpp
#include "test1.h"
void fun2()    { cout << g_str << endl;    }
```

以上test1和test2可以同时编译连接通过，g_str是整个工程的全局变量，在内存中只存在一份。

有些人喜欢把全局变量的声明和定义放在一起，这样可以防止忘记了定义，如把上面test1.h改为：

```c++
//test1.h
extern char g_str[] = "123456"; // 这个时候相当于没有extern
```

然后把test1.cpp中的g_str的定义去掉,这个时候再编译连接test1和test2两个模块时，会报连接错误，这是因为test1.cpp和test2.cpp都包含了test1.h，所以定义了两次g_str,这个时候连接器就会报错r。如果你非要把g_str的定义放在test1.h中的话，那么就把test2的代码中#include "test1.h"去掉 换成:

```c++
//test2.cpp
extern char g_str[];
void fun2()   {  cout << g_str << endl;   }
```

这个时候编译器就知道g_str是引自于外部的一个编译模块了，不会在本模块中再重复定义一个出来，但是十分不推荐这样做。头文件的作用就是要给外部提供接口使用的，所以请记住，**只在头文件中做声明**。

### extern和 static

extern 表明该变量在别的地方已经定义过了，在这里要使用那个变量。

static 表示静态的变量，分配内存的时候，存储在静态区,不存储在栈上面。

static 作用范围是内部连接的关系,，和extern有点相反。它和对象本身是分开存储的,extern也是分开存储的,但是extern可以被其他的对象用extern 引用,而static 不可以,只允许对象本身用它. 具体差别首先，static与extern是一对“水火不容”的家伙，也就是说extern和static不能同时修饰一个变量；其次，static修饰的全局变量声明与定义同时进行，也就是说当你在头文件中使用static声明了全局变量后，它也同时被定义了；最后，static修饰全局变量的作用域只能是本身的编译单元，也就是说它的“全局”只对本编译单元有效，其他编译单元则看不到它,如:

```c++
//test1.h:
#ifndef TEST1H
#define TEST1H
static char g_str[] = "123456"; 
void fun1();
#endif
```

```c++
//test1.cpp:
#include "test1.h"
void fun1()  {   cout << g_str << endl;  }
```

```c++
//test2.cpp
#include "test1.h"
void fun2()  {   cout << g_str << endl;  }
```

以上两个编译单元可以连接成功, 当你打开test1.obj时，你可以在它里面找到字符串"123456",同时你也可以在test2.obj中找到它们，它们之所以可以连接成功而没有报重复定义的错误是因为虽然它们有相同的内容，但是存储的物理地址并不一样，就像是两个不同变量赋了相同的值一样，而这两个变量分别作用于它们各自的编译单元。正是因为static有以上的特性，所以一般定义static全局变量时，都把它放在原文件中而不是头文件，这样就不会给其他模块造成不必要的信息污染。

### extern和const

C++中const修饰的全局常量据有跟static相同的特性，即它们只能作用于本编译模块中，但是const可以与extern连用来声明该常量可以作用于其他编译模块中, 如extern const char g_str[];
然后在原文件中定义:     const char g_str[] = "123456"; 

所以当const单独使用时它就与static相同，而当与extern一起合作的时候，它的特性就跟extern的一样了。

### 参考

[C/C++中extern关键字详解](http://www.cnblogs.com/yc_sunniwell/archive/2010/07/14/1777431.html)



## new与malloc

### new和malloc的内存分配

new是分配在自由存储区而malloc分配在堆上，自由存储区可以是堆也可以不是，具体要看new内部的实现。操作系统在堆上维护一个空闲内存链表，当需要分配内存的时候，就查找这个表，找到一块内存大于所需内存的区域，分配内存并将剩余的内存空间返还到空闲链表上（如果有剩余的话）。

### new/delete和malloc/free的区别

- malloc和free是库函数，而new和delete是C++操作符；



- new自己计算需要的空间大小，比如 int * a = new，malloc需要指定大小，例如 int * a = malloc(sizeof(int))；

- new在动态分配内存的时候可以初始化对象，调用其构造函数，delete在释放内存时调用对象的析构函数。而malloc只分配一段给定大小的内存，并返回该内存首地址指针，如果失败，返回NULL。

- new是C++操作符，是关键字，而operate new是库函数；opeartor new /operator delete可以重载，而malloc不行


- 对于数据C++定义new[]专门进行动态数组分配，用delete[]进行销毁。new[]会一次分配内存，然后多次调用构造函数；delete[]会先多次调用析构函数，然后一次性释放。


```c++
//分配数组不同之处
int char* pa = new char[100];
int char* pb = malloc(sizeof(char) * 100);
```

- malloc能够直观地重新分配内存


使用malloc分配的内存后，如果在使用过程中发现内存不足，可以使用realloc函数进行内存重新分配实现内存的扩充。realloc先判断当前的指针所指内存是否有足够的连续空间，如果有，原地扩大可分配的内存地址，并且返回原来的地址指针；如果空间不够，先按照新指定的大小分配空间，将原有数据从头到尾拷贝到新分配的内存区域，而后释放原来的内存区域。 
new没有这样直观的配套设施来扩充内存。

new和malloc内部实现的区别

以下是从网上找来的一段关于new的代码，不知道和标准的实现是否有区别，但是原理应该是这样，足够来说明问题了：

```c++
void *__CRTDECL operator new(size_t size) _THROW1(_STD bad_alloc) {    // try to allocate size bytes  
	void *p;  
	while ((p = malloc(size)) == 0)  
		if (_callnewh(size) == 0)  {     // report no memory  
			_THROW_NCEE(_XSTD bad_alloc, );
		}  

	return (p);  
}
```

new: 可以理解成两步： 

1. 调用operate new（）分配内存，如果内存不足失败，抛出异常； 
2. 如果需要的话，在那段内存上初始化对象(赋值或者调用构造函数），这个应该是由编译器根据代码来控制的。

因此对于new和malloc检查是否正确分配的方法是不一样的

```c++
int *a  = (int *)malloc ( sizeof (int ));
if(NULL == a){
	...
} else {
	...
}

try {
	int *a = new int();
} catch (std::bad_alloc& e) {
    ...
}
```

为了照顾原来习惯的程序员，C++可以通过nothrow关键字来实现new不抛异常而是返回NULL。

```c++
int* p = new(std::nothrow) int;
```

### malloc的实现

当我们调用malloc分配n个字节的空间时，实际上占用了n + sizeof(mem_control_block)个字节的空间。但是返回的地址是紧跟结构体mem_control_block后面的第一个地址。那么相信聪明的你已经猜到了free是如何释放内存的了。没错，就是把指针往回倒个sizeof(mem_control_block)的距离，然后设置标志位为可用。为了减少内存碎片，会查找前面一个块和后面一个块，如果有空闲块就合并为一个。

> 给free()中的参数就可以完成释放工作！这里要追踪到malloc()的申请问题了。申请的时候实际上占用的内存要比申请的大。因为超出的空间是用来记录对这块内存的管理信息。先看一下在《UNIX环境高级编程》中第七章的一段话：
>
> 大多数实现所分配的存储空间比所要求的要稍大一些，额外的空间用来记录管理信息——分配块的长度，指向下一个分配块的指针等等。这就意味着如果写过一个已分配区的尾端，则会改写后一块的管理信息。这种类型的错误是灾难性的，但是因为这种错误不会很快就暴露出来，所以也就很难发现。将指向分配块的指针向后移动也可能会改写本块的管理信息。

### 参考

[new与malloc的前世今生](http://www.cnblogs.com/amanlikethis/p/3765908.html)

版权声明：本文为博主原创文章，未经博主允许不得转载。



## 堆和栈

### 程序的内存分配

  一个由C/C++编译的程序占用的内存分为以下几个部分： 

1. 栈区（stack）—   由编译器自动分配释放   ，存放函数的参数值，局部变量的值等。其操作方式类似于数据结构中的栈。  
2. 堆区（heap）   —   一般由程序员分配释放，   若程序员不释放，程序结束时可能由OS回收   。注意它与数据结构中的堆是两回事，分配方式倒是类似于链表，呵呵。  
3. 全局区（静态区）（static）—  全局变量和静态变量的存储是放在一块的，初始化的全局变量和静态变量在一块区域，   未初始化的全局变量和未初始化的静态变量在相邻的另一块区域。   -   程序结束后由系统释放。  
4. 文字常量区   —常量字符串就是放在这里的。   程序结束后由系统释放  
5. 程序代码区—存放函数体的二进制代码。  



```c++
// main.cpp    
int a = 0; // 全局初始化区    
char *p1; // 全局未初始化区    
int main() {    
	int b; // 栈
	char s[] = "abc"; // 栈
	char *p2; // 栈
	char *p3 = "123456"; // 123456/0在常量区，p3在栈上。
	static int c = 0；// 全局（静态）初始化区
	p1 = (char *)malloc(10);
	p2 = (char *)malloc(20);
	//分配得来得10和20字节的区域就在堆区。
	strcpy(p1, "123456");   // 123456/0放在常量区，编译器可能会将它与p3所指向的"123456"优化成一个地方。
	return 1
}
```



### 堆和栈的理论知识

#### 申请方式

stack: 由系统自动分配。例如，声明在函数中一个局部变量  int b; 系统自动在栈中为b开辟空间

heap: 需要程序员自己申请，并指明大小，在c中malloc函数，如p1   =   (char   *)malloc(10);  在C++中用new运算符，如p2   =   new   char[10]; 但是注意p1、p2本身是在栈中的。

#### 申请后系统响应

栈：只要栈的剩余空间大于所申请空间，系统将为程序提供内存，否则将报异常提示栈溢出。

堆：首先应该知道操作系统有一个记录空闲内存地址的链表，当系统收到程序的申请时，会遍历该链表，寻找第一个空间大于所申请空间的堆结点，然后将该结点从空闲结点链表中删除，并将该结点的空间分配给程序，另外，对于大多数系统，会在这块内存空间中的首地址处记录本次分配的大小，这样，代码中的delete语句才能正确的释放本内存空间。另外，由于找到的堆结点的大小不一定正好等于申请的大小，系统会自动的将多余的那部分重新放入空闲链表中。

#### 申请大小限制

栈：在Windows下,栈是向低地址扩展的数据结构，是一块连续的内存的区域。这句话的意思是栈顶的地址和栈的最大容量是系统预先规定好的，在WINDOWS下，栈的大小是2M（也有的说是1M，总之是一个编译时就确定的常数），如果申请的空间超过栈的剩余空间时，将提示overflow。因此，能从栈获得的空间较小。

堆：堆是向高地址扩展的数据结构，是不连续的内存区域。这是由于系统是用链表来存储的空闲内存地址的，自然是不连续的，而链表的遍历方向是由低地址向高地址。堆的大小受限于计算机系统中有效的虚拟内存。由此可见，堆获得的空间比较灵活，也比较大。

#### 申请效率

栈由系统自动分配，速度较快。但程序员是无法控制的。堆是由new分配的内存，一般速度比较慢，而且容易产生内存碎片,不过用起来最方便。另外，在WINDOWS下，最好的方式是用VirtualAlloc分配内存，他不是在堆，也不是在栈是直接在进程的地址空间中保留一块内存，虽然用起来最不方便。但是速度快，也最灵活。

#### 存储内容

栈：在函数调用时，第一个进栈的是主函数中后的下一条指令（函数调用语句的下一条可执行语句）的地址，然后是函数的各个参数，在大多数的C编译器中，参数是由右往左入栈的，然后是函数中的局部变量。注意静态变量是不入栈的。当本次函数调用结束后，局部变量先出栈，然后是参数，最后栈顶指针指向最开始存的地址，也就是主函数中的下一条指令，程序由该点继续运行。堆：一般是在堆的头部用一个字节存放堆的大小。堆中的具体内容由程序员安排。

#### 存取效率

```c++
char s1[] = "aaaaaaaaaaaaaaa";
char *s2 = "bbbbbbbbbbbbbbbbb";
```

aaaaaaaaaaa是在运行时刻赋值的；而bbbbbbbbbbb是在编译时就确定的；但是，在以后的存取中，在栈上的数组比指针所指向的字符串(例如堆)快。

比如：

```c++
#include    
void main() {
	char a = 1;
	char c[] = "1234567890";
	char *p = "1234567890";
	a = c[1];
	a = p[1];
	return;
}   
```

第一种在读取时直接就把字符串中的元素读到寄存器cl中，而第二种则要先把指针值读到edx中，再根据edx读取字符，显然慢了。

#### 小结

堆和栈的区别可以用如下的比喻来看出：使用栈就象我们去饭馆里吃饭，只管点菜（发出申请）、付钱、和吃（使用），吃饱了就走，不必理会切菜、洗菜等准备工作和洗碗、刷锅等扫尾工作，他的好处是快捷，但是自由度小。使用堆就象是自己动手做喜欢吃的菜肴，比较麻烦，但是比较符合自己的口味，而且自由度大。   (经典！)  

### 参考

[堆和栈的区别（转过无数次的文章](http://blog.csdn.net/hairetz/article/details/4141043)



## 多态性

### 基本概念

多态性可以简单地概括为“一个接口，多种方法”，程序在运行时才决定调用的函数，它是面向对象编程领域的核心概念。多态(polymorphism)，字面意思多种形状。

C++多态性是通过虚函数来实现的，虚函数允许子类重新定义成员函数，而子类重新定义父类的做法称为覆盖(override)，或者称为重写。（这里我觉得要补充，重写的话可以有两种，直接重写成员函数和重写虚函数，只有重写了虚函数的才能算作是体现了C++多态性）而重载则是允许有多个同名的函数，而这些函数的参数列表不同，允许参数个数不同，参数类型不同，或者两者都不同。编译器会根据这些函数的不同列表，将同名的函数的名称做修饰，从而生成一些不同名称的预处理函数，来实现同名函数调用时的重载问题。但这并没有体现多态性。

多态与非多态的实质区别就是函数地址是早绑定还是晚绑定。如果函数的调用，在编译器编译期间就可以确定函数的调用地址，并生产代码，是静态的，就是说地址是早绑定的。而如果函数调用的地址不能在编译器期间确定，需要在运行时才确定，这就属于晚绑定。

那么多态的作用是什么呢，封装可以使得代码模块化，继承可以扩展已存在的代码，他们的目的都是为了代码重用。而多态的目的则是为了接口重用。也就是说，不论传递过来的究竟是那个类的对象，函数都能够通过同一个接口调用到适应各自对象的实现方法。

最常见的用法就是声明基类的指针，利用该指针指向任意一个子类对象，调用相应的虚函数，可以根据指向的子类的不同而实现不同的方法。如果没有使用虚函数的话，即没有利用C++多态性，则利用基类指针调用相应的函数的时候，将总被限制在基类函数本身，而无法调用到子类中被重写过的函数。因为没有多态性，函数调用的地址将是一定的，而固定的地址将始终调用到同一个函数，这就无法实现一个接口，多种方法的目的了。笔试题目：

```c++
#include<iostream>
using namespace std;
class A  {
public:
	void foo() {
    	printf("1\n");
    }
    virtual void fun() {
    	printf("2\n");
    }
};
class B : public A  {
public:
	void foo() {
		printf("3\n");
	}
	void fun() {
		printf("4\n");
	}
};

int main(void)  {
	A a;
	B b;
	A *p = &a;
	p->foo();
	p->fun();
	p = &b;
	p->foo();
	p->fun();
	return 0;
} 
```

第一个p->foo()和p->fuu()都很好理解，本身是基类指针，指向的又是基类对象，调用的都是基类本身的函数，因此输出结果就是1、2。

第二个输出结果就是1、4。p->foo()和p->fuu()则是基类指针指向子类对象，正式体现多态的用法，p->foo()由于指针是个基类指针，指向是一个固定偏移量的函数，因此此时指向的就只能是基类的foo()函数的代码了，因此输出的结果还是1。而p->fun()指针是基类指针，指向的fun是一个虚函数，由于每个虚函数都有一个虚函数列表，此时p调用fun()并不是直接调用函数，而是通过虚函数列表找到相应的函数的地址，因此根据指向的对象不同，函数地址也将不同，这里将找到对应的子类的fun()函数的地址，因此输出的结果也会是子类的结果4。

笔试的题目中还有一个另类测试方法。即

```
B *ptr = (B *)&a;  ptr->foo();  ptr->fun();
```

问这两调用的输出结果。这是一个用子类的指针去指向一个强制转换为子类地址的基类对象。结果，这两句调用的输出结果是3，2。

并不是很理解这种用法，从原理上来解释，由于B是子类指针，虽然被赋予了基类对象地址，但是ptr->foo()在调用的时候，由于地址偏移量固定，偏移量是子类对象的偏移量，于是即使在指向了一个基类对象的情况下，还是调用到了子类的函数，虽然可能从始到终都没有子类对象的实例化出现。

而ptr->fun()的调用，可能还是因为C++多态性的原因，由于指向的是一个基类对象，通过虚函数列表的引用，找到了基类中fun()函数的地址，因此调用了基类的函数。由此可见多态性的强大，可以适应各种变化，不论指针是基类的还是子类的，都能找到正确的实现方法。

```c++
#include<iostream>
using namespace std;
class Base  {
public:
	virtual void f(float x) {
		cout<<"Base::f(float)"<< x <<endl;
	}
	void g(float x) {
		cout<<"Base::g(float)"<< x <<endl;
	}
	void h(float x) {
		cout<<"Base::h(float)"<< x <<endl;
	}
};
class Derived : public Base {
public:
	virtual void f(float x) {
		cout<<"Derived::f(float)"<< x <<endl;   //多态、覆盖
	}
	void g(int x) {
		cout<<"Derived::g(int)"<< x <<endl;     //隐藏
	}
	void h(float x)	{
		cout<<"Derived::h(float)"<< x <<endl;   //隐藏
	}
};
int main(void) {
	Derived d;
	Base *pb = &d;
	Derived *pd = &d; // Good : behavior depends solely on type of the object
	pb->f(3.14f);   // Derived::f(float) 3.14
	pd->f(3.14f);   // Derived::f(float) 3.14
	// Bad : behavior depends on type of the pointer
	pb->g(3.14f);   // Base::g(float)  3.14
	pd->g(3.14f);   // Derived::g(int) 3
	// Bad : behavior depends on type of the pointer
	pb->h(3.14f);   // Base::h(float) 3.14
	pd->h(3.14f);   // Derived::h(float) 3.14
	return 0;
}
//小结：
// 1、有virtual才可能发生多态现象
// 2、不发生多态（无virtual）调用就按原类型调用
```


本来仅仅区别重载与覆盖并不算困难，但是C++的隐藏规则使问题复杂性陡然增加。
这里“隐藏”是指派生类的函数屏蔽了与其同名的基类函数，规则如下：

- 如果派生类的函数与基类的函数同名，但是参数不同。此时，不论有无virtual关键字，基类的函数将被隐藏（注意别与重载混淆）。
- 如果派生类的函数与基类的函数同名，并且参数也相同，但是基类函数没有virtual关键字。此时，基类的函数被隐藏（注意别与覆盖混淆）。

上面的程序中：

（1）函数Derived::f(float)覆盖了Base::f(float)。

（2）函数Derived::g(int)隐藏了Base::g(float)，而不是重载。

（3）函数Derived::h(float)隐藏了Base::h(float)，而不是覆盖。

### C++纯虚函数

#### 定义

  纯虚函数是在基类中声明的虚函数，它在基类中没有定义，但要求任何派生类都要定义自己的实现方法。在基类中实现纯虚函数的方法是在函数原型后加“=0” 
  virtual void funtion()=0 

#### 引入原因

为了方便使用多态特性，我们常常需要在基类中定义虚拟函数。 在很多情况下，基类本身生成对象是不合情理的。例如，动物作为一个基类可以派生出老虎、孔雀等子类，但动物本身生成对象明显不合常理。 

为了解决上述问题，引入了纯虚函数的概念，将函数定义为纯虚函数（方法：virtual ReturnType Function()= 0;），则编译器要求在派生类中必须予以重写以实现多态性。同时含有纯虚拟函数的类称为抽象类，它不能生成对象。这样就很好地解决了上述两个问题。

#### 相似概念

多态性：指相同对象收到不同消息或不同对象收到相同消息时产生不同的实现动作。C++支持两种多态性：编译时多态性，运行时多态性。 
**  a、编译时多态性：通过重载函数实现   b、运行时多态性：通过虚函数实现。 **

虚函数：虚函数是在基类中被声明为virtual，并在派生类中重新定义的成员函数，可实现成员函数的动态覆盖（Override）

抽象类：包含纯虚函数的类称为抽象类。由于抽象类包含了没有定义的纯虚函数，所以不能定义抽象类的对象



## 类型转换

### 显式类型转换

“强制类型转换”(cast)
C     风格： (type-id)
C++风格： **static_cast**、**dynamic_cast**、**reinterpret_cast**、和**const_cast**

### static_cast

用法：**static_cast **< type-id > ( expression )

说明：该运算符把expression转换为type-id类型，但没有运行时类型检查来保证转换的安全性。

来源：为什么需要static_cast强制转换？
情况1：void指针->其他类型指针
情况2：改变通常的标准转换
情况3：避免出现可能多种转换的歧义

它主要有如下几种用法：

- 用于类层次结构中基类和子类之间指针或引用的转换。进行上行转换（把子类的指针或引用转换成基类表示）是安全的；进行下行转换（把基类指针或引用转换成子类指针或引用）时，由于没有动态类型检查，所以是不安全的。
- 用于基本数据类型之间的转换，如把int转换成char，把int转换成enum。这种转换的安全性也要开发人员来保证。
- 把void指针转换成目标类型的指针(不安全!!)
- 把任何类型的表达式转换成void类型。

注意：static_cast不能转换掉expression的const、volitale、或者__unaligned属性。

### dynamic_cast

用法：**dynamic_cast **< type-id > ( expression )

说明：该运算符把expression转换成type-id类型的对象。Type-id必须是类的指针、类的引用或者void *；如果type-id是类指针类型，那么expression也必须是一个指针，如果type-id是一个引用，那么expression也必须是一个引用。

来源：为什么需要dynamic_cast强制转换？
简单的说，当无法使用virtual函数的时候

dynamic_cast主要用于类层次间的上行转换和下行转换，还可以用于类之间的交叉转换。

在类层次间进行上行转换时，dynamic_cast和static_cast的效果是一样的；在进行下行转换时，dynamic_cast具有类型检查的功能，比static_cast更安全。

```c++
class Base {
public:
    int m_iNum;
    virtual void foo();
};

class Derived:public Base {
public:
    char *m_szName[100];
};

void func(Base *pb) {
    Derived *pd1 = static_cast<Derived *>(pb);
    Derived *pd2 = dynamic_cast<Derived *>(pb);
}
```

在上面的代码段中，如果pb实际指向一个Derived类型的对象，pd1和pd2是一样的，并且对这两个指针执行Derived类型的任何操作都是安全的；如果pb实际指向的是一个Base类型的对象，那么pd1将是一个指向该对象的指针，对它进行Derived类型的操作将是不安全的（如访问m_szName），而pd2将是一个空指针(即0，因为dynamic_cast失败)。

另外要注意：Base要有虚函数，否则会编译出错；static_cast则没有这个限制。这是由于运行时类型检查需要运行时类型信息，而这个信息存储在类的虚函数表（关于虚函数表的概念，详细可见<Inside c++ object model>）中，只有定义了虚函数的类才有虚函数表，没有定义虚函数的类是没有虚函数表的。

另外，**dynamic_cast**还支持交叉转换（cross cast）。如下代码所示。

```c++
class Base {
public:
    int m_iNum;
    virtual void f(){};
};
class Derived1 : public Base { };
class Derived2 : public Base { };

void foo() {
    derived1 *pd1 = new Drived1;
    pd1->m_iNum = 100;
    Derived2 *pd2 = static_cast<Derived2 *>(pd1); //compile error
    Derived2 *pd2 = dynamic_cast<Derived2 *>(pd1); //pd2 is NULL
    delete pd1;
}
```

在函数foo中，使用**static_cast**进行转换是不被允许的，将在编译时出错；而使用 **dynamic_cast**的转换则是允许的，结果是空指针。

### reinpreter_cast

用法：**reinpreter_cast**<type-id> (expression)

说明：type-id必须是一个指针、引用、算术类型、函数指针或者成员指针。它可以把一个指针转换成一个整数，也可以把一个整数转换成一个指针（先把一个指针转换成一个整数，在把该整数转换成原类型的指针，还可以得到原先的指针值）。

### const_cast

用法：**const_cast**<type_id> (expression)

说明：该运算符用来修改类型的const或volatile属性。除了const 或volatile修饰之外， type_id和expression的类型是一样的。

常量指针被转化成非常量指针，并且仍然指向原来的对象；常量引用被转换成非常量引用，并且仍然指向原来的对象；常量对象被转换成非常量对象。

```c++
class B {
public:
    int m_iNum;
}

void foo(){
    const B b1;
    b1.m_iNum = 100; //comile error
    B b2 = const_cast<B>(b1);
    b2. m_iNum = 200; //fine
}
```

上面的代码编译时会报错，因为b1是一个常量对象，不能对它进行改变；使用const_cast把它转换成一个常量对象，就可以对它的数据成员任意改变。注意：b1和b2是两个不同的对象。

### 参考

[C++中static_cast, dynamic_cast, const_cast用法/使用情况及区别解析](http://blog.csdn.net/bzhxuexi/article/details/17021559)



## 内存管理

### 内存分配方式

在C++中，内存分成5个区，他们分别是堆、栈、自由存储区、全局/静态存储区和常量存储区。
**栈**：在执行函数时，函数内局部变量的存储单元都可以在栈上创建，函数执行结束时这些存储单元自动被释放。栈内存分配运算内置于处理器的指令集中，效率很高，但是分配的内存容量有限。
**堆**：就是那些由 `new`分配的内存块，他们的释放编译器不去管，由我们的应用程序去控制，一般一个`new`就要对应一个 `delete`。如果程序员没有释放掉，那么在程序结束后，操作系统会自动回收。
**自由存储区**：就是那些由`malloc`等分配的内存块，他和堆是十分相似的，不过它是用`free`来结束自己的生命的。
**全局/静态存储区**：全局变量和静态变量被分配到同一块内存中，在以前的C语言中，全局变量又分为初始化的和未初始化的，在C++里面没有这个区分了，他们共同占用同一块内存区。
**常量存储区**：这是一块比较特殊的存储区，他们里面存放的是常量，不允许修改。



首先，我们举一个例子：

```c++
void f() { int* p=new int[5]; }
```

这条短短的一句话就包含了堆与栈，看到`new`，我们首先就应该想到，我们分配了一块堆内存，那么指针`p`呢？他分配的是一块栈内存，所以这句话的意思就是：在栈内存中存放了一个指向一块堆内存的指针`p`。在程序会先确定在堆中分配内存的大小，然后调用`operator new`分配内存，然后返回这块内存的首地址，放入栈中。

### 控制C++的内存分配

在嵌入式系统中使用C++的一个常见问题是内存分配，即对`new` 和 `delete` 操作符的失控。具有讽刺意味的是，问题的根源却是C++对内存的管理非常的容易而且安全。具体地说，当一个对象被消除时，它的析构函数能够安全的释放所分配的内存。

这当然是个好事情，但是这种使用的简单性使得程序员们过度使用`new` 和 `delete`，而不注意在嵌入式C++环境中的因果关系。并且，在嵌入式系统中，由于内存的限制，频繁的动态分配不定大小的内存会引起很大的问题以及堆破碎的风险。

但当你必须要使用`new`和`delete`时，你不得不控制C++中的内存分配。你需要用一个全局的`new` 和`delete`来代替系统的内存分配符，并且一个类一个类的重载`new`和`delete`。一个防止堆破碎的通用方法是从不同固定大小的内存持中分配不同类型的对象。对每个类重载`new` 和`delete`就提供了这样的控制。

#### 重载全局的new和delete操作符

可以很容易地重载new 和 delete 操作符，如下所示:

```c++
void * operator new(size_t size){
    void *p = malloc(size);
    return (p);
}

void operator delete(void *p){
    free(p);
}
```

这段代码可以代替默认的操作符来满足内存分配的请求。出于解释C++的目的，我们也可以直接调用`malloc()` 和`free()`。也可以对单个类的`new` 和 `delete`操作符重载。这是你能灵活的控制对象的内存分配。

```
class TestClass {
    public:
    void * operator new(size_t size);
    void operator delete(void *p);
    // .. other members here ...
};

void *TestClass::operator new(size_t size){
    void *p = malloc(size); // Replace this with alternative allocator
    return (p);
}

void TestClass::operator delete(void *p){
    free(p); // Replace this with alternative de-allocator
}
```

所有`TestClass` 对象的内存分配都采用这段代码。更进一步，任何从`TestClass` 继承的类也都采用这一方式，除非它自己也重载了`new` 和 `delete` 操作符。通过重载`new` 和 `delete` 操作符的方法，你可以自由地采用不同的分配策略，从不同的内存池中分配不同的类对象。

### 常见的内存错误及其对策

发生内存错误是件非常麻烦的事情。编译器不能自动发现这些错误，通常是在程序运行时才能捕捉到。而这些错误大多没有明显的症状，时隐时现，增加了改错的难度。 常见的内存错误及其对策如下：

- 内存分配未成功，却使用了它。编程新手常犯这种错误，因为他们没有意识到内存分配会不成功。常用解决办法是，在使用内存之前检查指针是否为`NULL`。如果指针`p`是函数的参数，那么在函数的入口处用`assert(p!=NULL)`进行检查。如果是用`malloc`或`new`来申请内存，应该用`if(p==NULL)` 或`if(p!=NULL)`进行防错处理。
- 内存分配虽然成功，但是尚未初始化就引用它。犯这种错误主要有两个起因：一是没有初始化的观念；二是误以为内存的缺省初值全为零，导致引用初值错误（例如数组）。
- 内存分配成功并且已经初始化，但操作越过了内存的边界。例如在使用数组时经常发生下标“多1”或者“少1”的操作。特别是在`for`循环语句中，循环次数很容易搞错，导致数组操作越界。
- 忘记了释放内存，造成内存泄露。含有这种错误的函数每被调用一次就丢失一块内存。刚开始时系统的内存充足，看不到错误。终有一次程序突然死掉，系统提示：内存耗尽。动态内存的申请与释放必须配对，程序中`malloc`与`free`的使用次数一定要相同（`new/delete`同理）。
- 释放了内存却继续使用它。

### 指针与数组的对比

C++/C程序中，指针和数组在不少地方可以相互替换着用，但是两者并不等价。
数组要么在静态存储区被创建（如全局数组），要么在栈上被创建。数组名对应着（而不是指向）一块内存，其地址与容量在生命期内保持不变，只有数组的内容可以改变。
指针可以随时指向任意类型的内存块，它的特征是“可变”，所以我们常用指针来操作动态内存。指针远比数组灵活，但也更危险。

下面示例中，字符数组a的容量是6个字符，其内容为 hello。a的内容可以改变，如`a[0]= ‘X’`。指针p指向常量字符串“world”（位于静态存储区，内容为world），常量字符串的内容是不可以被修改的。从语法上看，编译器并不觉得语句`p[0]= ‘X’`有什么不妥，但是该语句企图修改常量字符串的内容而导致运行错误。

```c++
char a[] = “hello”;
a[0] = ‘X’;
cout << a << endl;
char *p = “world”; // 注意p指向常量字符串
p[0] = ‘X’; // 编译器不能发现该错误
cout << p << endl;
```

不能对数组名进行直接复制与比较。若想把数组a的内容复制给数组b，不能用语句 `b = a` ，否则将产生编译错误。应该用标准库函数`strcpy`进行复制。同理，比较b和a的内容是否相同，不能用`if(b==a)` 来判断，应该用标准库函数`strcmp`进行比较。

语句 `p = a` 并不能把a的内容复制指针p，而是把a的地址赋给了p。要想复制a的内容，可以先用库函数`malloc`为p申请一块容量为`strlen(a)+1`个字符的内存，再用`strcpy`进行字符串复制。同理，语句`if(p==a)` 比较的不是内容而是地址，应该用库函数`strcmp`来比较。

```c++
// 数组…
char a[] = "hello";
char b[10];
strcpy(b, a); // 不能用 b = a;
if(strcmp(b, a) == 0) // 不能用 if (b == a)
// 指针…
int len = strlen(a);
char *p = (char *)malloc(sizeof(char)*(len+1));
strcpy(p,a); // 不要用 p = a;
if(strcmp(p, a) == 0) // 不要用 if (p == a)
```

#### 计算内存容量

用运算符`sizeof`可以计算出数组的容量（字节数）。如下示例中，`sizeof(a)`的值是12（注意别忘了’’）。指针p指向a，但是`sizeof(p)`的值却是4。这是因为`sizeof(p)`得到的是一个指针变量的字节数，相当于`sizeof(char*)`，而不是p所指的内存容量。C++/C语言没有办法知道指针所指的内存容量，除非在申请内存时记住它。

```
char a[] = "hello world";
char *p = a;
cout<< sizeof(a) << endl; // 12字节
cout<< sizeof(p) << endl; // 4字节
```

注意当数组作为函数的参数进行传递时，该数组自动退化为同类型的指针。如下示例中，不论数组a的容量是多少，`sizeof(a)`始终等于`sizeof(char *)`。

```
void Func(char a[100]){
    cout<< sizeof(a) << endl; // 4字节而不是100字节
}
```

### 指针参数是如何传递内存的

如果函数的参数是一个指针，不要指望用该指针去申请动态内存。如下示例中，Test函数的语句`GetMemory(str, 200)`并没有使`str`获得期望的内存，`str`依旧是`NULL`，为什么？

```c++
void GetMemory(char *p, int num){
    p = (char *)malloc(sizeof(char) * num);
}

void Test(void){
    char *str = NULL;
    GetMemory(str, 100); // str 仍然为 NULL
    strcpy(str, "hello"); // 运行错误
}
```

毛病出在函数`GetMemory`中。编译器总是要为函数的每个参数制作临时副本，指针参数p的副本是 `_p`，编译器使 `_p=p`。如果函数体内的程序修改了`_p`的内容，就导致参数p的内容作相应的修改。这就是指针可以用作输出参数的原因。在本例中，`_p`申请了新的内存，只是把 `_p`所指的内存地址改变了，但是p丝毫未变。所以函数`GetMemory`并不能输出任何东西。事实上，每执行一次`GetMemory`就会泄露一块内存，因为没有用`free`释放内存。

如果非得要用指针参数去申请内存，那么应该改用“指向指针的指针”，见示例：

```c++
void GetMemory2(char **p, int num){
    *p = (char *)malloc(sizeof(char) * num);
}

void Test2(void){
    char *str = NULL;
    GetMemory2(&str, 100); // 注意参数是 &str，而不是str
    strcpy(str, "hello");
    cout<< str << endl;
    
    free(str);
}
```

我们可以用函数返回值来传递动态内存。这种方法更加简单，见示例：

```c++
char *GetMemory3(int num){
    char *p = (char *)malloc(sizeof(char) * num);
    return p;
}

void Test3(void){
    char *str = NULL;
    str = GetMemory3(100);
    strcpy(str, "hello");
    cout<< str << endl;
    free(str);
}
```

用函数返回值来传递动态内存这种方法虽然好用，但是常常有人把`return`语句用错了。这里强调不要用`return`语句返回指向“栈内存”的指针，因为该内存在函数结束时自动消亡，见示例：

```c++
char *GetString(void){
    char p[] = "hello world";
    return p; // 编译器将提出警告
}

void Test4(void){
    char *str = NULL;
    str = GetString(); // str 的内容是垃圾
    cout<< str << endl;
}
```

用调试器逐步跟踪`Test4`，发现执行`str = GetString`语句后`str`不再是`NULL`指针，但是`str`的内容不是`“hello world”`而是垃圾。

### 杜绝“野指针”

“野指针”不是`NULL`指针，是指向“垃圾”内存的指针。人们一般不会错用`NULL`指针，因为用`if`语句很容易判断。但是“野指针”是很危险的，`if`语句对它不起作用。 “野指针”的成因主要有三种：

(1). 指针变量没有被初始化。任何指针变量刚被创建时不会自动成为NULL指针，它的缺省值是随机的，它会乱指一气。所以，指针变量在创建的同时应当被初始化，要么将指针设置为NULL，要么让它指向合法的内存。例如：

```c++
char *p = NULL;
char *str = (char *) malloc(100);
```

(2). 指针p被free或者delete之后，没有置为NULL，让人误以为p是个合法的指针。

(3). 指针操作超越了变量的作用域范围。这种情况让人防不胜防。

### 内存耗尽怎么办

　　如果在申请动态内存时找不到足够大的内存块，`malloc`和`new`将返回`NULL`指针，宣告内存申请失败。通常有三种方式处理“内存耗尽”问题。
　　(1). 判断指针是否为`NULL`，如果是则马上用`return`语句终止本函数。

　　(2). 判断指针是否为`NULL`，如果是则马上用`exit(1)`终止整个程序的运行。

　　(3). 为`new`和`malloc`设置异常处理函数。例如Visual C++可以用`_set_new_hander`函数为`new`设置用户自己定义的异常处理函数，也可以让`malloc`享用与`new`相同的异常处理函数。

　　上述 (1)、(2) 方式使用最普遍。如果一个函数内有多处需要申请动态内存，那么方式 (1) 就显得力不从心（释放内存很麻烦），应该用方式 (2) 来处理。
　　有一个很重要的现象要告诉大家。对于32位以上的应用程序而言，无论怎样使用`malloc与new`，几乎不可能导致“内存耗尽”。

### 参考

[C/C++内存管理详解](https://chenqx.github.io/2014/09/25/Cpp-Memory-Management/)



## 排序算法

排序算法是最基本最常用的算法，不同的排序算法在不同的场景或应用中会有不同的表现，我们需要对各种排序算法熟练才能将它们应用到实际当中，才能更好地发挥它们的优势。今天，来总结下各种排序算法。

下面这个表格总结了各种排序算法的复杂度与稳定性：

![img](http://upload-images.jianshu.io/upload_images/273973-19cf4a1e58b6ebaf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/700)

各种排序算法复杂度比较

### 冒泡排序

冒泡排序可谓是最经典的排序算法了，它是基于比较的排序算法，时间复杂度为O(n^2)，其优点是实现简单，n较小时性能较好。

- 算法原理
  相邻的数据进行两两比较，小数放在前面，大数放在后面，这样一趟下来，最小的数就被排在了第一位，第二趟也是如此，如此类推，直到所有的数据排序完成

- c++代码实现

  ```c++
  void bubble_sort(int arr[], int len) {
  	for (int i = 0; i < len - 1; i++) {
  		for (int j = len - 1; j > i; j--) {
  			if (arr[j] < arr[j - 1]) {
  				int temp = arr[j];
  				arr[j] = arr[j - 1];
  				arr[j - 1] = temp;
  			}
  		}
  	}
  }
  ```

### 选择排序

- 算法原理
  先在未排序序列中找到最小（大）元素，存放到排序序列的起始位置，然后，再从剩余未排序元素中继续寻找最小（大）元素，然后放到已排序序列的末尾。以此类推，直到所有元素均排序完毕。

- c++代码实现

  ```c++
  void select_sort(int arr[], int len) {
      for (int i = 0; i < len; i++) {
          int index = i;
          for (int j = i + 1; j < len; j++) {
              if (arr[j] < arr[index])
                  index = j;
          }
          if (index != i) {
              int temp = arr[i];
              arr[i] = arr[index];
              arr[index] = temp; 
          }
      }
  }
  ```

### 插入排序

- 算法原理
  将数据分为两部分，有序部分与无序部分，一开始有序部分包含第1个元素，依次将无序的元素插入到有序部分，直到所有元素有序。插入排序又分为直接插入排序、二分插入排序、链表插入等，这里只讨论直接插入排序。它是**稳定**的排序算法，时间复杂度为O(n^2)

- c++代码实现

  ```c++
  void insert_sort(int arr[], int len) {
      for (int i = 1; i < len; i ++) {
          int j = i - 1;
          int k = arr[i];
          while (j > -1 && k < arr[j] ) {
              arr[j + 1] = arr[j];
              j --;
          }
          arr[j + 1] = k;
      }
  }
  ```

### 快速排序

- 算法原理
  快速排序是目前在实践中非常高效的一种排序算法，它不是稳定的排序算法，平均时间复杂度为O(nlogn)，最差情况下复杂度为O(n^2)。它的基本思想是：通过一趟排序将要排序的数据分割成独立的两部分，其中一部分的所有数据都比另外一部分的所有数据都要小，然后再按此方法对这两部分数据分别进行快速排序，整个排序过程可以递归进行，以此达到整个数据变成有序序列。
- c++代码实现

```c++
void quick_sort(int arr[], int left, int right) {
	if (left < right) {
		int i = left, j = right, target = arr[left];
		while (i < j) {
			while (i < j && arr[j] > target)
				j--;
			if (i < j)
				arr[i++] = arr[j];
			while (i < j && arr[i] < target)
				i++;
			if (i < j)
				arr[j] = arr[i];
    	}
    	arr[i] = target;
    	quick_sort(arr, left, i - 1);
    	quick_sort(arr, i + 1, right);
	}
}
```

### 归并排序

- 算法原理
  归并排序具体工作原理如下（假设序列共有n个元素）：

  - 将序列每相邻两个数字进行归并操作（merge)，形成floor(n/2)个序列，排序后每个序列包含两个元素
  - 将上述序列再次归并，形成floor(n/4)个序列，每个序列包含四个元素
  - 重复步骤2，直到所有元素排序完毕

  归并排序是稳定的排序算法，其时间复杂度为O(nlogn)，如果是使用链表的实现的话，空间复杂度可以达到O(1)，但如果是使用数组来存储数据的话，在归并的过程中，需要临时空间来存储归并好的数据，所以空间复杂度为O(n)

- c++代码实现

  ```c++
  void merge(int arr[], int temp_arr[], int start_index, int mid_index, int end_index) {
      int i = start_index, j = mid_index + 1;
      int k = 0;
      while (i < mid_index + 1 && j < end_index + 1) {
          if (arr[i] > arr[j])
              temp_arr[k++] = arr[j++];
          else
              temp_arr[k++] = arr[i++];
      }
      while (i < mid_index + 1)
          temp_arr[k++] = arr[i++];
      while (j < end_index + 1)
          temp_arr[k++] = arr[j++];
      for (i = 0, j = start_index; j < end_index + 1; i ++, j ++)
          arr[j] = temp_arr[i];
  }
  void merge_sort(int arr[], int temp_arr[], int start_index, int end_index) {
      if (start_index < end_index) {
          int mid_index = (start_index + end_index) / 2;
          merge_sort(arr, temp_arr, start_index, mid_index);
          merge_sort(arr, temp_arr, mid_index + 1, end_index);
          merge(arr, temp_arr, start_index, mid_index, end_index);
      }
  }
  ```

### 堆排序

#### 二叉堆

二叉堆是完全二叉树或者近似完全二叉树，满足两个特性

- 父结点的键值总是大于或等于(小于或等于)任何一个子节点的键值
- 每个结点的左子树和右子树都是一个二叉堆

当父结点的键值总是大于或等于任何一个子节点的键值时为最大堆。当父结点的键值总是小于或等于任何一个子节点的键值时为最小堆。一般二叉树简称为堆。

#### 堆的存储

一般都是数组来存储堆，`i`结点的父结点下标就为`(i – 1) / 2`。它的左右子结点下标分别为`2 * i + 1`和`2 * i + 2`。如第0个结点左右子结点下标分别为1和2。存储结构如图所示：

![img](http://upload-images.jianshu.io/upload_images/273973-d6e77b92c0a85ce5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/610)

堆结构

#### 堆排序原理

堆排序的时间复杂度为O(nlogn)

- 算法原理（以最大堆为例）


- 先将初始数据R[1..n]建成一个最大堆，此堆为初始的无序区
- 再将关键字最大的记录R[1]（即堆顶）和无序区的最后一个记录R[n]交换，由此得到新的无序区R[1..n-1]和有序区R[n]，且满足R[1..n-1].keys≤R[n].key
- 由于交换后新的根R[1]可能违反堆性质，故应将当前无序区R[1..n-1]调整为堆。
- 重复2、3步骤，直到无序区只有一个元素为止。


- c++代码实现

```c++
/**
 * 将数组arr构建大根堆
 * @param arr 待调整的数组
 * @param i   待调整的数组元素的下标
 * @param len 数组的长度
 */
void heap_adjust(int arr[], int i, int len) {
    int child;
    int temp;

    for (; 2 * i + 1 < len; i = child) {
        child = 2 * i + 1;  // 子结点的位置 = 2 * 父结点的位置 + 1
        // 得到子结点中键值较大的结点
        if (child < len - 1 && arr[child + 1] > arr[child])
            child ++;
        // 如果较大的子结点大于父结点那么把较大的子结点往上移动，替换它的父结点
        if (arr[i] < arr[child]) {
            temp = arr[i];
            arr[i] = arr[child];
            arr[child] = temp;
        } else break;
    }
}

/**
 * 堆排序算法
 */
void heap_sort(int arr[], int len) {
    int i;
    // 调整序列的前半部分元素，调整完之后第一个元素是序列的最大的元素
    for (int i = len / 2 - 1; i >= 0; i--)
        heap_adjust(arr, i, len);

    for (i = len - 1; i > 0; i--) {
        // 将第1个元素与当前最后一个元素交换，保证当前的最后一个位置的元素都是现在的这个序列中最大的
        int temp = arr[0];
        arr[0] = arr[i];
        arr[i] = temp;
        // 不断缩小调整heap的范围，每一次调整完毕保证第一个元素是当前序列的最大值
        heap_adjust(arr, 0, i);
    }
}
```



### 参考

[各种排序算法总结](http://www.jianshu.com/p/f5baf7f27a7e)



## STL数据结构

### 简介

List封装了链表,Vector封装了数组, list和vector得最主要的区别在于vector使用连续内存存储的，他支持[]运算符，而list是以链表形式实现的，不支持[]。

Vector对于随机访问的速度很快，但是对于插入尤其是在头部插入元素速度很慢，在尾部插入速度很快。List对于随机访问速度慢得多，因为可能要遍历整个链表才能做到，但是对于插入就快的多了，不需要拷贝和移动数据，只需要改变指针的指向就可以了。另外对于新添加的元素，Vector有一套算法，而List可以任意加入。
Map,Set属于标准关联容器，使用了非常高效的平衡检索二叉树：红黑树，他的插入删除效率比其他序列容器高是因为不需要做内存拷贝和内存移动，而直接替换指向节点的指针即可。
Set和Vector的区别在于Set不包含重复的数据。Set和Map的区别在于Set只含有Key，而Map有一个Key和Key所对应的Value两个元素。
Map和Hash_Map的区别是Hash_Map使用了Hash算法来加快查找过程，但是需要更多的内存来存放这些Hash桶元素，因此可以算得上是采用空间来换取时间策略。

#### **vector**

向量 相当于一个数组，在内存中分配一块连续的内存空间进行存储。支持不指定vector大小的存储。STL内部实现时，首先分配一个非常大的内存空间预备进行存储，即capacituy（）函数返回的大小，当超过此分配的空间时再整体重新放分配一块内存存储，这给人以vector可以不指定vector即一个连续内存的大小的感觉。通常此默认的内存分配能完成大部分情况下的存储。

优点：

1. 不指定一块内存大小的数组的连续存储，即可以像数组一样操作，但可以对此数组进行动态操作。通常体现在push_back() pop_back()
2. 随机访问方便，即支持[ ]操作符和vector.at()
3. 节省空间。

缺点：

1. 在内部进行插入删除操作效率低。
2. 只能在vector的最后进行push和pop，不能在vector的头进行push和pop。
3. 当动态添加的数据超过vector默认分配的大小时要进行整体的重新分配、拷贝与释放 

#### **list**

双向链表，每一个结点都包括一个信息快Info、一个前驱指针Pre、一个后驱指针Post。可以不分配必须的内存大小方便的进行添加和删除操作。使用的是非连续的内存空间进行存储。
优点：

1. 不使用连续内存完成动态操作。
2. 在内部方便的进行插入和删除操作
3. 可在两端进行push、pop

缺点：

1. 不能进行内部的随机访问，即不支持[ ]操作符和vector.at()
2. 相对于verctor占用内存多

#### **deque**

双端队列 double-end queue，deque是在功能上合并了vector和list。
优点：

1. 随机访问方便，即支持[ ]操作符和vector.at()
2. 在内部方便的进行插入和删除操作
3. 可在两端进行push、pop

缺点：

1. 占用内存多

#### **使用区别**

1. 如果你需要高效的随即存取，而不在乎插入和删除的效率，使用vector 
2. 如果你需要大量的插入和删除，而不关心随即存取，则应使用list 
3. 如果你需要随即存取，而且关心两端数据的插入和删除，则应使用deque

 STL 特性：前闭后开

 

### 参考

[c++ list, vector, map, set 区别与用法比较](http://www.cnblogs.com/smiler/p/4457622.html)