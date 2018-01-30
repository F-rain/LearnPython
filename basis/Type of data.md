# Python基本数据类型
- 整数
- 浮点数
- 字符串

    单引号或者双引号括起来的任意文本。文本内的单，双引号用\做转义。

- 布尔值

    布尔值可以用and，or，not来运算。分别代表与，或，非运算

- 空值

    none是Python里面的空值。None不能理解为0。0有意义，而None代表特殊的空值。
# 变量
变量名必须是由大小写英文，数字和_的组合。且不能用数字开头。
# 常量
常量通常用大写字母来命名。Python没有任何机制保证常量不被改变。所谓的常量只是一种约定俗称的习惯。
# list and tuple
- list

    Python里内置的一种数据类型——列表。list是一个有序集合，可以随时添加或删除其中的元素。
    
        //初始化一个list，并把他付给classmate。
        classmate = ['li', 'ma', 'rain'] 
        //获取list的元素个数。
        len(classmate) 

        //用索引来访问其中的元素
        classmate[0] //访问第一个元素
        .
        .
        .
        classmate[-1] //访问最后一个元素
        .
        .
        .

        //追加元素
        classmate.append('rick')
        //插入元素
        classmate.insert(1,'wang')//把元素插入到索引为1的位置
        //删除元素
        classmate.pop() //删除最后一个元素
        classmate.pop(i) //删除索引为i的元素
    list中的元素可以是不同的数据类型。也可是是另一个list。
- tuple

    元组。和list非常类似。但tuple元素一旦初始化就不可改变。
    
        //初始化一个元组
        classmates = ('li', 'ma', 'rain')
    tuple陷阱：因为不可变，所以定义的时候就需要把元素确定下来。

        t = (1, 2, 3)
        //空tuple
        t = ()
        //只有一个元素的tuple
        t = (1,)//为了消除把t=(1)理解成为t=1的歧义。
    “可变”的tuple
    
        t = ('a', 'b', ['A', 'B'])
    在tuple中存一个list元素。tuple虽然不可变，但是list可变。表面上tuple中的A和B是可以被重新赋值变化的。但其实变化的是list中的元素。tuple本身并没有变化。