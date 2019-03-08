# constructors in c++

当你声明了一个类之后，如果你没有初始化，是不可以使用里面的变量的。因此我们需要用初始函数初始化对象，C++ 类的初始函数有专门的写法。

C++ 的类必须要有初始化函数，当然 C++ 有默认的初始函数，但是只负责分配空间，而 JAVA 会自动设置变量为零。所以，初始函数最好自己写。

初始函数可以重载，也就是可以有多个初始函数，区别在于参数不一样。

初始函数一定是公开的，不然会出错。

 