# struct和class差异
- struct中的成员是公有的
- class中的成员是私有的
    - **class 可以实现被继承,构造函数和析构函数**


# 通用的链表，通过struct 实现 
``` 
typedef struct tagST_LIST
{
    
  //  struct tagST_LIST *pri ;  
    struct tagST_LIST *next ;  

}ST_LIST ; 
```  


# 空类
- 一个空类编译默认会创建4个成员函数，构造函数，析构函数，

# class 中初始化问题
- 常量的初始化要在构造函数中执行 
- 或者的类中声明定义成员时，采用static const int a  = 0 ;  

# 注意重载和多态的区别
- 重载是单纯的重新加载
- 多态是将同一个接口函数，实现不同的任务。


# 虚拟继承 
- 目前也不怎么使用，为了应对多层继承中，内存的使用问题，以及换乱问题。
- A基类B继承了，A也被C继承了， 那么D同时继承C和B的时候，就会有多出2个A的继承，
此时D到底是哪个A？ 如果B和C都是虚拟继承那就会有这问题了。

# 虚函数和虚继承的关系
- 虚函数是为了实现多态而存在
- 这样可也不用在每个类中都重载和实现

# **C++中所有的继承默认都是私有继承的** 

