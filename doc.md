[TOC]

# Setting Up Your Environment

鉴于我给这篇文档的定位应该是及其初学者友好的，就让我们从构建编程环境开始吧！ Let's go!

## First step

我们先下载最流行的 Python distribution: Anaconda. 点击链接跳转官网：[https://www.anaconda.com](https://www.anaconda.com/)

Python 流行的发行版本有很多，但我们强烈推荐此版本，为什么呢？我们知道，Python 的强大之处不仅仅在于其语言之灵活与严谨（至少对比别的统计软件要严谨得多，尽管习惯了 C/C++ 或者其它强类型语言的人往往对 Python 的“不严谨”感到不适），还在于其庞大的开发者社区以及众多可用的拓展包。下载 Python 的核心编译器是很简单的，但是构建一个完整的开发环境远不止这一点。我们还要管理这些拓展包、建造一个舒适的 coding 界面、使用其它开发工具并进行互动等。而这些琐事对初学者来说是不友好而且很没必要的。因此我们选择一个集大成者————对它就是 Anaconda！

Anaconda 提供的功能非常强大！但其中许多功能对入门 Python 不是必要的，我们仅介绍下文中会一直使用的 Jupiter Notebook ，其它功能就等待大家的探索啦！

## Jupiter

Python 是解释型语言，用人话来说就是我们可以一边 coding 一边执行，一边构造自己的思路一边看运行结果，这不同于 C++ 等编译型语言，总要等编译器从头到尾编译一遍，生成可执行文件（*.exe）再运行之查看结果。这就为交互式编程提供了可能，Jupiter Notebook 就是这样一个交互式编程界面。交互式编程界面到底是什么样呢？看看本文档你就知道了。这篇文档是全部用 Jupiter Notebook 写的，一边写程序，一边码文档。

在安装好 Anaconda 之后， Jupiter 会自动安装，你可以在自己的程序列表里找到他。打开之后会自动跳出浏览器， Jupiter便成功运行了。如果你总觉得界面看起来有点奇怪，那可能是浏览器的问题，建议使用谷歌浏览器。

请找到一个合适的工作目录， New 一个 Python3 Notebook ，可以开始编程之旅了。想要更多 Jupiter 的信息，这些网站可能会提供帮助。

## About Python

### 解释型语言

前面提到了 Python 是一种解释型语言，现在介绍一个后文会经常提到的概念——**解释器（interpreter）**。解释器就是负责把你敲出的 code 转换成真正计算器能够理解的机器语言的工具。它一面是用户友好型的高级语言，一面是计算机友好的机器语言。

### 简单的语法结构

Python 饱受争议的一点就是它简单的语法结构。Python 的解释器通过缩进（所谓的缩进就是四个空格）来辨认代码中的各个代码块，这和其它编程语言很不一样。由于缩进被用来确定代码块，因此 Python 的缩进是非常严格的。什么时候应该缩进，而什么时候不应该，都需要根据你想实现的功能来确定，不能像其它语言一样想缩到那里去就缩到哪里去。但总是敲四个空格很麻烦，幸运的是现在许多文档编辑器都提供了自动替换功能，即把 TAB 自动替换为四个空格，从此你就可以通过只按以下 TAB 键来实现缩进了。

### 简单的数据类型

尽管相比统计软件来说，Python 需要我们严肃对待各个变量的数据的类型，但相比更经典的 C/C++ 或者其它一些语言来说，Python 仍然能够被称为“弱类型语言”。因为 Python 这门语言的设计目的就是能够让我们更方便的写程序，而逃离过多形式化的限制。例如在 Python 中创建一个整数类型的数据，我们只要说它是一个整数，而不用说明是占内存8字节的整数还是16字节的整数，正如我们在 C++ 中做的那样。

## 使用建议

想必你已经体会到了，在阅读的过程中经常会不可避免地遇到一些难以理解的专有名词（尽管我已经尽量减少他们的出现或者伴以通俗易懂的解释），这时候请尽管忽视它们，我们在后续的学习中会慢慢接触并熟悉这些工具。当然如果你有兴趣的话，那就善用搜索引擎吧。有一个值得推荐的开发者互动社区，stackoverflow：[https://stackoverflow.com](https://stackoverflow.com/)


# Python Essentials

这章主要介绍了一些编程的基础，更多的是一些描述性内容。

## Overview

- 数据类型
- 包的导入
- 基础的文件读写操作
- 迭代
- 友好的函数操作
- 逻辑运算符

## 数据类型

在编程的时候要和许多对象打交道，正如日常生活中我们会给事物分类一样，在 Python 的编程过程中，我们也给遇到的任何对象进行分类。

### 基础类型

- 布尔型：只取 是/非 、 0/1 等非此即彼的数据类型
- 整数：和数学中的定义相同
- 浮点数：也就是数学中定义的有理数、实数等需要电脑进行近似估计的数。这种数据电脑无法精确表示，只能在某一个精度基础上近似表达。在通常意义上电脑的计算精度一般都足够高，使得我们可以把它当成精确的数值来看。
- 字符串：单纯地把一串字符连在一起而已。

以下示例是上述数据类型的赋值：


```python
x1 = True # 布尔型
x2 = 1 # 整数型
x3 = 1.1 # 浮点型
x4 = 'string' # 利用单引号表示字符串

print(type(x1)) # Type() 函数会返回输入对象的数据类型，print用于输出
print(type(x2))
print(type(x3))
print(type(x4))
```

    <class 'bool'>
    <class 'int'>
    <class 'float'>
    <class 'str'>
    

我们可以看到上面有

### 容器类型

正如其字面意义，容器类型意味着这种数据类型本身可以容纳其它数据。

- 列表（list）：可以对内容进行修改
- 元组（tuple）：作为一整个固定的对象，不可修改

Python 的特性之一是其容器类型可以同时容纳不同类型的数据。


```python
list1 = [1, 2, 3] # 使用中括号构建列表
print(type(list1))

tuple1 = (1, 2, 3)
print(type(tuple1))
```

    <class 'list'>
    <class 'tuple'>
    


```python
list1[0] # 可以使用中括号访问列表的内容，序数参数从0开始基数；元组也一样
```




    1




```python
list1[0] = 'New data' 
list1 # 从输出可以看书列表支持不同的类型；并且列表的内部元素是可以被修改的
```




    ['New data', 2, 3]




```python
tuple1[0] = 'New data' # 元组的内部元素不可以修改；在编程时要注意返回的错误信息哦
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-10-599a6d9bf824> in <module>()
    ----> 1 tuple1[0] = 'New data' # 元组的内部元素不可以修改；在编程时要注意返回的错误信息哦
    

    TypeError: 'tuple' object does not support item assignment


#### Slice notation

切片记号……直译听起来比较奇怪，直观上来说就是可以通过一些记号更便捷地对列表/元组的数据进行防卫，其概念类似 Matlab 的分号表达式。通过例子来说明吧：


```python
a = [2, 4, 6, 8]
a[1:] # 从第一位一直访问到结束；注意这里的序号是从0开始计数的
```




    [4, 6, 8]




```python
a[1:3] # a[m, n] 从第 m 位开始访问；共输出 n-m 位
```




    [4, 6]




```python
a[-2:] # 从倒数第二位输出到结束
```




    [6, 8]



其实这些记号是不需要硬背的，只需要记住一个原则就好了。

a.[m: n] 其中m代表开始输出的位置（该位置上的数输出）；n代表停止输出的位置（该位置上的数不输出），如果前面有负号就倒着算，如果其中一个为空就说明解释器不知道从哪里开始/停止，只好从第一/最后一位开始/停止。

令人惊讶的是，上述记号全都能用在字符串上！为什么呢？其实很好理解，字符串相当于一系列单个字符的集合，在某种意义上相当于一个不可改变的列表，也就是元组，那么访问的记号自然也就一样了

### 集合和字典

这当然就是数学定义中的集合啦！还记得对集合的定义吗，不可以出现相同元素，这里也一样。除此之外数学中可以对集合进行的各种运算也一并被移植到 Python 的基础语法中了。而字典类型正如我们学习中用到的字典一样，它包含关键字段以及对其的解释语段。



```python
set1 = {'a', 'b', 'a'} # 使用花括号创建集合
print(type(set1))

set2 = {'b'}
set2.issubset(set1) # 判断集合的包含关系；其他集合运算可以通过百度查询
```

    <class 'set'>
    




    True




```python
dic1 = {'name': 'Frodo', 'age': 33} # 使用匹配的一组数据创建字典

# 我们好奇，字典的关键字（key）能否重复呢？
dic2 = {'name': 'Frodo', 'age': 33, 'age': 30}
dic2['age']
```




    30



我们可以看到关键字居然是可以重复的。其实从另一方面来说，可以理解为解释器在处理这条语句的时候是顺序处理的；在处理到最后一句的时候并不是创建了一个相同的关键字，只是发现了一个新的数据然后覆盖掉了之前存过的数据。

## 包的导入

前面也说过， Python 的强大之处在于它有非常多可用的包（library or module），现在我们就来尝试使用他们。



```python
import math # 导入一个名字为 math 的包，正如其名，它提供了许多数学计算工具

math.sqrt(4) # 这里举了个栗子， math 中有一个负责开根的工具，在导入 math 包之后可以直接使用
```




    2.0



当然导入方式不只一种：


```python
from math import * # 直译就是从 math 包中导入一切；在这种方式下不需要通过 . 访问 math 中的方法

sqrt(4)
```




    2.0



上面这种方式是不推荐的，因为一个包中往往有多到数不清的方法/函数可供使用，直接导入到当前的工作环境会导致命名冲突


```python
import math as ma # 我们还可以为导入的包取一个别名；这样写起来更方便
```

## 文件IO

Python 可以进行各种文件读写操作，我们先从简单的开始，


```python
f = open('newfile.txt', 'w') # 打开一个新的文件； 'w' 意味着可以写入（write）
f.write('Testing\n') # 这一部分是写入文件的内容
f.write('Testing again') # 紧接着又写了一部分
f.close() # 关闭文件
```

在每次进行文件读写操作之后都要记得关闭文件，这是为了防止在其它部分程序的运行中对文件进行误操作，关闭了文件之后就不用担心这个问题了。

现在我们来看看怎么从文件中读取数据：


```python
f = open('newfile.txt', 'r') # 打开一个新文件； 'r' 意味着可以读取（read）
out = f.read() # 我们把读出来的内容保存到变量 out 中
out # 查看 out 中的内容
```




    'Testing\nTesting again'



### 路径操作（Paths）

上面讲了文件IO，由于读写文件涉及对电脑硬盘上某个具体位置的文件进行操作，这就涉及 Python 工作路径的问题。我们可以很容易的获取、设置当前路径，只需要借助 OS （operation system）包。


```python
import os
print(os.getcwd()) # 输出当前工作路径
```

    C:\Users\hyiku\Python
    

备注：Magic command 是一个很好用的东西，可以很方便地进行涉及操作系统的操作。其中很多命令都和 Linux 系统中的命令类似，熟悉 Linux 的同学可以很好地上手。

## 迭代

迭代指的是计算机中某种重复进行的操作，例如循环。我们先介绍实现循环的一些指令，具体内部实现机制在之后的章节中会陆续详细介绍，


```python
x_values = [1,2,3] # 这是一个元素为常数的列表
for x in x_values:
    print(x * x)
```

    1
    4
    9
    

这就是 for 循环。

## Exercise 1


```python
import numpy as np
import matplotlib as plt
```

### Part 1


```python
x_values = [np.random.uniform() for i in range(100)]
y_values = [np.random.uniform() for i in range(100)]
inner_prdt = 0
for x,y  in zip(x_values, y_values):
    inner_prdt += x*y
```


```python
inner_prdt
```




    23.880626305708333



### Part 2


```python
sum(i%2 for i in range(100))
```




    50



### Part 3


```python
pairs = ((2, 5), (4, 2), (9, 8), (12, 10))
```


```python
len(pairs) - sum((x%2 or y%2) for x, y in pairs)
```




    2



## Exercise 2


```python
def p(x, coeff):
    return sum(coe*x**i for i, coe in enumerate(coeff))
```


```python
coeff = [1, 1, 1]
x = 2
p(x, coeff)
```




    7



## Exercise 3


```python
def f(string):
    count = 0
    for letter in string:
        if letter == letter.upper() and letter.isalpha():
            count += 1
    return count
```




    3



上面通过直接调用系统内的包实现，但是对于编程而言应该知道背后的逻辑


```python
def num_cap(string):
    return sum(ord(x)>=65 and ord(x)<=90 for x in string)
```


```python
num_cap('aaabbbA')
```




    1



## Exercise 4


```python
def f(seq_a, seq_b):
    is_subset = True
    for a in seq_a:
        if a not in seq_b:
            is_subset = False
    return is_subset
```


```python
def judge(a, b):
    key1 = True
    for i in a:
        key2 = False
        for j in b:
            if i == j:
                key2 = True 
        if not key2:
            key1 = False
    return key1
```


```python
a = 'acbeccd'
b = 'abcd'
judge(a, b)
```




    False



## Exercise 5


```python
def linapprox(f, a, b, n, x):
    step = (b-a)/(n-1)
    u, v = int((x-a)/step)*step+a, (int((x-a)/step)+1)*step+a
    return f(u) + (x - u) * (f(v) - f(u)) / (v - u)
```


```python
def test(f, a, b, n, x):
    length_of_interval = b - a
    num_subintervals = n - 1
    step = length_of_interval / num_subintervals
    point = a
    while point <= x:
        point += step
    u, v = point - step, point
    return f(u) + (x - u) * (f(v) - f(u)) / (v - u)
```


```python
a = 0
b = 10
f = lambda x: x**3
n = 10
```


```python
test(f, a, b, n, 4.5)
```




    91.97530864197532




```python
linapprox(f, a, b, n, 4.5)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-1-bab74053684e> in <module>()
    ----> 1 linapprox(f, a, b, n, 4.5)
    

    NameError: name 'linapprox' is not defined


# Matplotlib


```python
import matplotlib.pyplot as plt
import numpy as np
fig, ax = plt.subplots()
x = np.linspace(0, 10, 200)
y = np.sin(x)
ax.plot(x, y, 'b-', linewidth=2)
plt.show()
```


![png](output_60_0.png)



```python

```
