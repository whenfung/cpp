# C++  header files

C++ 不同于Java，它有一种叫头文件的东西，头文件用来函数声明。

前面我们讲过编译器，如果找不到函数的声明，编译就会失败。如果将函数声明都放到头文件里，我们需要的时候引用，那么预处理的时候会将其合并，编译就会成功，这就是头文件的作用。 

在 VS 创建头文件的时候，你会发现有一行叫 `#pragma once` 的代码，这段代码的意思是编译的时候源文件只被引入一次，这样就不会出现重定义的问题。当然我也看过有些人用 `#ifndif ` 来实现该功能，但是我更推荐使用 `#pragma once` 。

注意到很多 C++ 库，例如 `iostream`，不同于 C 语言的文件库，C++ 是没有后缀 `.h` 。

因为标准库非常的庞大，所以程序员在选择的类的名称或函数名时就很有可能和标准库中的某个名字相同。所以为了避免这种情况所造成的名字冲突，就把标准库中的一切都放在名字空间 std 中。但这又会带来了一个新问题。无数原有的 C++ 代码都依赖于使用了多年的伪标准库中的功能，他们都是在全局空间下的。所以就有了`<iostream.h>` 和 `<iostream>` 等等这样的头文件，一个是为了兼容以前的 C++ 代码，一个是为了支持新的标准。