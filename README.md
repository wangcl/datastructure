# data structure
data structure sample code written in different programming languages.



### 概念

- 数据

    描述客观事物的符号，是能被计算机识别并输入给计算机处理的符号集合。

    1. 可以输入到计算机中
    2. 能被计算机程序处理

- 数据元素

    是组成数据的、有一定意义的基本单位，在计算机中通常作为整体处理，也称为“记录”。

- 数据项

    一个数据元素可以由若干个数据项组成，数据项是数据不可分割的最小单位。

    *注：“数据项”是数据的最小单位，但“数据元素”才是数据结构中建立数据模型的基础*

- 数据对象

    性质相同的数据元素的集合，是数据的子集。

    *注：“性质相同”指数据元素具有相同数量和类型的数据项*

- 数据结构

    相互之间存在一种或多种特定关系的数据元素的集合。

### 逻辑结构

逻辑结构指数据对象中数据元素之间的相互关系。逻辑结构是针对**具体问题**的，是为了解决某个问题，在对问题理解的基础上，选择一个合适的数据结构表示数据元素之间的逻辑关系。

逻辑结构分为：

1. 集合结构

    集合结构中的数据元素除了同属于一个集合外，它们之间没有其他关系。各个数据元素是“平等”的，它们的共同属性是“同属于一个集合”。

2. 线性结构

    线性结构中的数据元素之间是“一对一”的关系。

3. 树形结构

    树形结构中的数据元素之间存在一种“一对多”的层次关系。

4. 图形结构

    图形结构的数据元素是“多对多”的关系。

### 物理结构

物理结构也叫做“存储结构”，是指数据的逻辑结构在计算机中的存储形式。数据是数据元素的集合，那么根据物理结构的定义，实际上就是如何把数据元素存储到计算机的存储器中。物理结构是面向**计算机**的，其基本的目标就是将数据及其逻辑关系存储到计算机的内存中。

数据元素的存储结构形式有两种：

1. 顺序存储结构

    把数据元素存放在地址连续的存储单元里，其数据间的逻辑关系和物理关系是一致的。

2. 链式存储结构

    把数据元素存放在任意的存储单元里，这组存储单元可以是连续的，也可以是不连续的。数据元素的存储关系并不能反映其逻辑关系，因此需要用一个指针存放数据元素的地址，这样通过地址就可以找到相关联数据元素的位置。

### 抽象数据类型（Abstract Data Type，ADT）

ADT是指一个数学模型及定义在该模型上的一组操作。抽象数据类型的定义仅取决于它的一组逻辑特性，而与其在计算机内部如何表示和实现无关。

```
ADT 
    抽象数据类型名
Data
    数据元素之间逻辑关系的定义
Operation
    操作1
        初始条件
        操作结果描述
    操作2
        ......
    操作n
        ......
endADT
```

### 算法

算法是解决特定问题求解步骤的描述，在计算机中表现为指令的有限序列，并且每条指令表示一个或多个操作。

算法具有五个基本特性：

1. 输入

    算法具有零个或多个输入。

2. 输出

    算法至少有一个或多个输出。

3. 有穷性

    算法在执行有限的步骤之后，自动结束而不会出现无限循环，并且每一个步骤在可接受的时间内完成。

4. 确定性

    算法的每一步骤都具有确定的含义，不会出现二义性。算法在一定条件下，只有一条执行路径，相同的输入只能有唯一的输出结果。算法的每个步骤被精确定义而无歧义。

5. 可行性

    算法的每一步都必须是可行的，也就是说，每一步都能够通过执行有限次数完成。可行性意味着算法可以转换为程序上机运行，并得到正确的结果。

算法设计的要求：

1. 正确性

    算法的正确性是指算法至少应该具有输入、输出和加工处理无歧义性、能正确反映问题的需求、能够得到问题的正确答案。

2. 可读性

    算法设计的另一目的是为了便于阅读、理解和交流。

3. 健壮性

    当输入数据不合法时，算法也能做出相关处理，而不是产生异常或莫名其妙的结果。

4. 时间效率高和存储量低

    时间效率指的是算法的执行时间，对于同一个问题，如果有多个算法能够解决，执行时间短的算法效率高，执行时间长的效率低。存储量需求指的是算法在执行过程中需要的最大存储空间，主要指算法程序运行时所占用的内存或外部硬盘存储空间。设计算法应该尽量满足时间效率高和存储量低的需求。

### 算法的时间复杂度（Big O）

在进行算法分析时，语句总的执行次数 `T(n)` 是关于问题规模n的函数，进而分析 `T(n)` 随n的变化情况并确定 `T(n)` 的数量级。算法的时间复杂度，也就是算法的时间量度，记作： `T(n)=O(f(n))` 。它表示随问题规模n的增大，算法执行时间的增长率和 `f(n)` 的增长率相同，称作**算法的渐近时间复杂度**，简称为**时间复杂度**。其中 `f(n)` 是问题规模n的某个函数。

推导大O阶的方法：

1. 用常数1取代运行时间中的所有加法常数
2. 在修改后的运行次数函数中，只保留最高阶项
3. 如果最高阶项存在且不是1，则去除与这个项相乘的常数

大O阶：

1. 常数阶 `O(1)`

    与问题的大小无关（n的多少），执行时间恒定的算法，我们称之为具有 `O(1)` 的时间复杂度，又叫常数阶。

2. 线性阶 `O(n)`

    ```c
    for (int i = 0; i < n; i++)
    {
        /* 时间复杂度为O(1)的程序步骤序列 */
    }
    ```

    线性阶包含循环。

3. 对数阶 `O(logn)`

    ```c
    int count = 1;
    while (count < n)
    {
        count = count * 2;
        /* 时间复杂度为O(1)的程序步骤序列 */
    }
    ```

    对数阶首先有循环条件，其次计数值以2的倍数变化。

4. 平方阶 O(n^2^)

    ```c
    int i, j;
    for (i = 0; i < n; i++)
    {
        for (j = 0; j < n; j++)
        {
            /* 时间复杂度为O(1)的程序步骤序列 */
        }
    }
    ```

    平方阶包含双重循环。

5. n(logn)阶

6. 立方阶 O(n^3^)

常用的时间复杂度所耗费的时间从小到大排列：

O(1) < O(logn) < O(n) < o(n^2^) < O(n^3^) < O(2^n^) < O(n!) < O(n^n^)

*注：从 O(n^3^) 起，过大的n都会使结果变得不现实，所以一般不讨论。*

对算法的分析，一种方法是计算所有情况的平均值，这种时间复杂度的计算方法称为平均时间复杂度。另一种方法是计算最坏情况下的时间复杂度，这种方法称为最坏时间复杂度。一般在没有特殊说明的情况下，都是指**最坏时间复杂度**。

