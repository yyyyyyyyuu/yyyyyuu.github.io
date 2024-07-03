# 第一天 Python的基础

## 第一节 初识Python及其开发环境

### 问题：

### 1.什么是Python？

### 2.为什么使用Python？

### 3.Python有什么作用？

### 任务：

### 完成环境安装



## 一、Python简介

### 1. 了解Python

Python是一种解释型（这意味着开发过程中没有了编译这个环节）、面向对象（支持面向对象的风格或代码封装在对象的编程技术）、动态数据类型的交互式（可在命令行中通过Python提示符及直接代码执行程序）高级程序设计语言。
![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQVbmjAX6ESW0SPvwzAPbHEzFuuq7nA6XParLWPxINCl7X5HOvMohwsA/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

### 2. Python介绍

Python是时下最流行、最火爆的编程语言，具体原因：

- 简单、易学，适应人群广泛
  ![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQiaeXo5bb3yXsm2LYA4Or9xUvRVRpwMS9uPh5znAu82BnJN3L0pSlkBQ/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)
- 免费、开源
- 应用领域广泛
  ![image-20240628140958492](.\pic\第一天\应用领域.png)

> 备注：以下知名框架均是Python语言开发。
>
> 1. Google开源机器学习框架：TensorFlow
> 2. 开源社区主推学习框架：Scikit-learn
> 3. 百度开源深度学习框架：Paddle

### 3. Python特点

1. 易于学习：Python有相对较少的关键字，结构简单，和一个明确定义的语法，学习起来更加简单。
2. 易于阅读：Python代码定义的更清晰。
3. 易于维护：Python的成功在于它的源代码是相当容易维护的。
4. 一个广泛的标准库：Python的最大的优势之一是丰富的库，跨平台的，在UNIX，Windows和Macintosh兼容很好。
5. 互动模式：互动模式的支持，您可以从终端输入执行代码并获得结果的语言，互动的测试和调试代码片断。
6. 可移植：基于其开放源代码的特性，Python已经被移植（也就是使其工作）到许多平台。
7. 可扩展：如果你需要一段运行很快的关键代码，或者是想要编写一些不愿开放的算法，你可以使用C或C++完成那部分程序，然后从你的Python程序中调用。
8. 数据库：Python提供所有主要的商业数据库的接口。
9. GUI编程：Python支持GUI可以创建和移植到许多系统调用。
10. 可嵌入: 你可以将Python嵌入到C/C++程序，让你的程序的用户获得"脚本化"的能力。

### 4. Python发展历史

Python发展历史：https://baike.baidu.com/item/Python/407313?fr=aladdin

### 5. Python版本

- Python 2.X (停止维护)
- Python 3.X

## 二、环境准备

### Python解释器

### 1. 解释器的作用

![python解释器的作用](.\pic\第一天\python解释器的作用.png)

- Python解释器作用：运行文件（1.翻译代码  2.提交给计算机运行）
- Python解释器种类
- - PyPy，基于Python语言开发的解释器。
  - Jython，运行在Java平台的解释器，直接把Python代码编译成Java字节码执行。
  - IronPython，运行在微软.Net平台上的Python解释器，可以直接把Python代码编译成.Net的字节码。
  - CPython，C语言开发的解释器[官方]，应用广泛的解释器。
  - IPython，基于CPython的一种交互式解释器。
  - 其他解释器

### 2. 解释器的安装

Python解释器的安装：https://blog.csdn.net/weixin_43495473/article/details/103559812

Python下载：https://www.python.org/downloads

### PyCharm安装

### 1. PyCharm的作用

PyCharm是一种Python IDE（集成开发环境），带有一整套可以帮助用户在使用Python语言开发时提高其效率的工具，内部集成的功能如下：

- Project管理
- 智能提示
- 语法高亮
- 代码跳转
- 调试代码
- 解释代码(解释器)
- 框架和库
- …

### 2. PyCharm安装与使用

PyCharm的安装：https://blog.csdn.net/weixin_43495473/article/details/103560198

PyCharm的下载：https://www.jetbrains.com/pycharm/download/

PyCharm破解：https://ziby0nwxdov.feishu.cn/docx/LnWldH37DoKTmxxIcCWcrIQEnoh

## 三、第一个Python程序

```python
print('人生苦短，我学Python')
```

![第一个python程序](.\pic\第一天\第一个python程序.png)

小练习：

![exercise01](.\pic\第一天\exercise01.png)

​     运气，无法抓在手中，总是可遇不可求；机缘，不能准确把握，总是找找又觅觅；成功，在于奋斗不息，总是充满希望。







# 第二节 Python基础语法

## 一、代码格式

### 1.注释

#### 1.1. 注释的作用

通过用自己熟悉的语言，在程序中对某些代码进行标注说明，这就是注释的作用，能够大大增强程序的可读性。

#### 1.2. 注释的分类及语法

注释分为两类：单行注释 和 多行注释。

- 单行注释

只能注释一行内容，语法如下：

```python
# 注释内容
```

- 多行注释

可以注释多行内容，一般用在注释一段代码的情况， 语法如下：

```python
"""  第一行注释  第二行注释  第三行注释"""
'''  注释1  注释2  注释3'''
```

> 快捷键： ctrl + /

**注意：解释器不执行任何的注释内容。**

### 2.缩进

Python代码的缩进可以通过Tab键控制，也可使用空格控制。空格是Python3首选的缩进方法，一般使用4个表示一级缩进；Python3不允许混合使用Tab和空格。

```python
if True:
    print ("True")
else:
    print ("False")
```

### 3.语句换行

Python官方建议每行代码不超过79个字符，若代码过长应该换行。Python会将**圆括号、中括号和大括号**中的行进行隐式连接，我们可以根据这个特点实现过长语句的换行显示。

```python
string = ("Python官方建议每行代码不超过79个字符，若代码过长应该换行。"
          "Python会将**圆括号、中括号和大括号**中的行进行隐式连接，"
          "我们可以根据这个特点实现过长语句的换行显示")
```



## 二、**变量**

### 1. 变量的作用

变量，简单来说，其实就是计算机内存中的一块储存空间，用来存储CPU需要使用的数据。而这个储存空间需要一个名字，这个名字的统称就叫变量。
![image-20240628150634823](.\pic\第一天\变量.png)
作用：

1. 用来临时保存数据
2. 便于项目的后期升级维护
3. 节约内存

### 2. 定义变量

```python
变量名 = 值
```

**变量名自定义，要满足标识符命名规则。**

#### 2.1 标识符

标识符命名规则是Python中定义各种名字的时候的统一规范，具体如下：

- 由数字、字母、下划线组成
- 不能数字开头
- 不能使用内置关键字
- 严格区分大小写

![关键字](.\pic\第一天\关键字.png)

#### 2.2 命名习惯

- 见名知义。
- 大驼峰：即每个单词首字母都大写，例如：`MyName`。
- 小驼峰：第二个（含）以后的单词首字母大写，例如：`myName`。
- 下划线：例如：`my_name`。

#### 2.3 使用变量

```python
my_name = "张三"
print(my_name)
myAge = 23
print(myAge)
```

## 三、数据类型

**在 Python 里为了应对不同的业务需求，也把数据分为不同的类型。**

![数据类型](.\pic\第一天\数据类型.png)

> 检测数据类型的方法：`type(变量名或者数值)`

```
a = 1
print(type(a))  # <class 'int'> -- 整型
b = 1.1
print(type(b))  # <class 'float'> -- 浮点型
c=3.14+90j    
print(type(c))  # <class 'complex'> --复数型
d = True
print(type(d))  # <class 'bool'> -- 布尔型
e = "12345"
print(type(e))  # <class 'str'> -- 字符串
f = [10, 20, 30]
print(type(f))  # <class 'list'> -- 列表
g = (10, 20, 30)
print(type(g))  # <class 'tuple'> -- 元组
h = {10, 20, 30}
print(type(h))  # <class 'set'> -- 集合
i = {"name": "张三", "age": 20}
print(type(i))  # <class 'dict'> -- 字典
```

思考：

1. 为什么Python会提出这么多种的数据类型?

> 有限的内存, 无限的变量, 合理的使用内存

   2.Python中，程序员定义变量需要关心变量的类型吗?

> - Python弱类型语言
> - 程序员不需要关心变量的类型, 只需要把数据书写正确即可，python会通过自动推到出您变量的类型。

## 四、输出

**作用：程序输出内容给用户。**

```
print('hello Python')
age = 18
print(age)
# 需求：输出“今年我的年龄是18岁”
```

print()函数用于向控制台中输出数据，它可以输出任何类型的数据，其语法格式如下所示：

```
print(*objects, sep=' ', end='\n', file=sys.stdout)

objects：表示输出的对象。输出多个对象时，对象之间需要用分隔符分隔。
sep：用于设定分隔符，默认使用空格作为分隔。
end：用于设定输出以什么结尾，默认值为换行符\n。
file：表示数据输出的文件对象。
```



### 1. 格式化输出

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQicOfpp4ArdgeXgJ7FaMzicf4GOojxibFMu4ib1ibV00fSUyZAHpHOVk8Rwg/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

> - %06d，表示输出的整数显示位数，不足以0补全，超出当前位数则原样输出。
> - %.2f，表示小数点后显示的小数位数。

### 2. 内置函数format

format()用于字符串格式化，功能非常强大，格式是str.format()，format函数可以接受不限个参数，位置可以不按顺序。

### 3. f-格式化字符串

f-string是格式化字符串的一种很好的新方法。与其他格式化方式相比，它不仅更易读，更简洁，不易出错，而且速度更快！格式为：`f'{表达式}'`。

### 4. 体验格式化字符串

```
name = "张三"
age = 23
weight = 75.5
student_id = 1
# 我的名字是张三
print('我的名字是%s' % name)
# 我的学号是0001
print('我的学号是%04d' % student_id)
# 我的体重是75.50公斤
print('我的体重是%.2f公斤' % weight)
# 我的名字是张三，今年23岁了
print('我的名字是%s，今年%d岁了' % (name, age))
# 我的名字是张三，明年24岁了
print('我的名字是%s，明年%d岁了' % (name, age + 1))
# 我的名字是张三，明年24岁了
print('我的名字是{0}, 明年{1}岁了'.format(name, age+1))
# 我的名字是李思，今年18岁了
print('我的名字是{0}, 今年{1}岁了'.format("李思", 18))
# 我的名字是张三，明年24岁了
print(f'我的名字是{name}, 明年{age + 1}岁了')
```

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQOjo9xx9D7UWZ0cUDZnQazibiaJQGh4dEWyyMuwys1gLftyB6VQjesHMQ/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

### 5. 补充知识

字符串输出的本质其实就是拼接字符串，那么我们都用`%s`完全也是可以的。很多时候，我们不用区分整型、浮点型等，直接用`%s`输出就可以了。

```
print('我的名字是%s，今年%s岁了，我的体重是%s公斤' % (name, age ,weight))
```

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQI9dEJWK6pTJ1pzlW3Bbc4cRibPqj0bfJY2SiaWrJ3XCibjLJryI4wTBqg/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

### 6. 转义字符

- `\n`：换行。
- `\t`：制表符，一个tab键（4个空格）的距离。

### 7. 结束符

```
# print会默认换行输出
print('输出的内容', end="\n")
```

> 在Python中，print()， 默认自带`end="\n"`这个换行结束符，所以导致每两个`print`直接会换行展示，用户可以按需求更改结束符。

```
# 改变Python换行输出
print('内容', end=" ")
print('内容', end="···")
```

## 八、输入

**在Python中，程序接收用户输入的数据的功能即是输入。**

![图片](.\pic\第一天\输入.png)

### 1. 输入的语法

```
input("提示信息")
```

### 2. 输入的特点

- 当程序执行到`input`，等待用户输入，输入完成之后才继续向下执行。
- 在Python中，`input`接收用户输入后，一般存储到变量，方便使用。
- 在Python中，`input`会把接收到的任意用户输入的数据都当做字符串处理。

```
password = input('请输入您的密码：')
print(f'您输入的密码是{password}')
print(type(password)) # <class 'str'>
```

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQklW6NxjXwaWYsrHbrcP4djK2NszvN0KFUg9XQEsoBuicjiccIcia5snFA/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

### 

## 十、运算符

### 1. 运算符的分类

- 算数运算符
- 赋值运算符
- 复合赋值运算符
- 比较运算符
- 逻辑运算符

### 2. 算数运算符

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQ9Bog7PQGdUfpTKyOum4LMnnicJQzP2A4icTXCNA5cW5XtUjasEdvD1zw/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

> 混合运算优先级顺序：`()`高于 `**` 高于 `*` `/` `//` `%` 高于 `+` `-`

### 3. 赋值运算符

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQF509PSIib2NTmuvskUp5CkH4RWVdhXlicfkiaCJhJibGicDdsO36vqPLMiag/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)



  1.单个变量赋值

```
num = 1
print(num)
```

2. 多个变量赋值

```
num1, float1, str1 = 10, 0.5, 'hello world'
print(num1)
print(float1)
print(str1)
```

3. 多变量赋相同值

```
a = b = 10
print(a)
print(b)
```



### 4. 复合赋值运算符

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQ5XEyGCMuOTgribUzT6Le8ick1sbA4E3VOONcunm9duoEwMVWkqxeJNnw/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

```
a = 100
a += 1
# 输出101  a = a + 1,最终a = 100 + 1
print(a)
b = 2
b *= 3
# 输出6  b = b * 3,最终b = 2 * 3
print(b)
c = 10
c += 1 + 2
# 输出13, 先算运算符右侧1 + 2 = 3， c += 3 , 推导出c = 10 + 3
print(c)
```

### 5. 比较运算符

**比较运算符也叫关系运算符， 通常用来判断。**

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQMq7pbpXD00jv6ibgNt3oCXtZeqndeicdKT0NEyc8qyNX1G4gzKLMZGJw/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

```
a = 7
b = 5
print(a == b)  # False
print(a != b)  # True
print(a < b)   # False
print(a > b)   # True
print(a <= b)  # False
print(a >= b)  # True
```

### 6. 逻辑运算符

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQk4tzoAZe8a3GAibcpE0x060C1ibpuBbrBSOUGb4q51lwAiaviaE9l3kJ4A/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

```
a = 1
b = 2
c = 3
print((a < b) and (b < c))  # True
print((a > b) and (b < c))  # False
print((a > b) or (b < c))   # True
print(not (a > b))          # True
```

### 7. 补充知识

数字之间的逻辑运算

```
a = 0
b = 1
c = 2

# and运算符，只要有一个值为0，则结果为0，否则结果为最后一个非0数字
print(a and b)  # 0
print(b and a)  # 0
print(a and c)  # 0
print(c and a)  # 0
print(b and c)  # 2
print(c and b)  # 1

# or运算符，只有所有值为0结果才为0，否则结果为第一个非0数字
print(a or b)  # 1
print(a or c)  # 2
print(b or c)  # 1
```

## 十一、条件语句

### 1. 了解条件语句

Python条件语句是通过一条或多条语句的执行结果（True或者False）来决定执行的代码块。

### 2. if语法

```
if 条件:
    条件成立执行的代码1
    条件成立执行的代码2
    ......
```

#### 2.1 体验if语句

```
if True:
    print('条件成立执行的代码1')
    print('条件成立执行的代码2')

# 下方的代码没有缩进到if语句块，所以和if条件无关
print('我是无论条件是否成立都要执行的代码')
```

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQGnWfDXfvrWwVZI3Epe3QXoDCHXlPicATHwX3jz6vJDGodeTTgRHHHxA/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

#### 2.2 简单版：网吧上网

需求分析：如果用户年龄大于等于18岁，即成年，输出"已经成年，可以上网"。

```
age = 20
if age >= 18:
    print('已经成年，可以上网')

print('系统关闭')
```

#### 2.3 进阶版：网吧上网

新增需求：用户可以输出自己的年龄，然后系统进行判断是否成年，成年则输出"您的年龄是’用户输入的年龄’，已经成年，可以上网"。

```
# input接受用户输入的数据是字符串类型，条件是age和整型18做判断，所以这里要int转换数据类型
age = int(input('请输入您的年龄：'))

if age >= 18:
    print(f'您的年龄是{age},已经成年，可以上网')


print('系统关闭')
```

### 3. if…else…

作用：条件成立执行if下方的代码; 条件不成立执行else下方的代码。

```
if 条件:
    条件成立执行的代码1
    条件成立执行的代码2
    ......
else:
    条件不成立执行的代码1
    条件不成立执行的代码2
    ......
```

> 思考：网吧上网的实例，如果成年，允许上网，如果不成年呢？是不是应该回复用户不能上网？

#### 3.1 实用版：网吧上网

```
age = int(input('请输入您的年龄：'))

if age >= 18:
    print(f'您的年龄是{age},已经成年，可以上网')
else:
    print(f'您的年龄是{age},未成年，请自行回家写作业')

print('系统关闭')
```

> 注意：如果条件成立执行了某些代码，那么其他的情况的代码将不会执行。

### 4. 多重判断

```

if 条件1:
    条件1成立执行的代码1
    条件1成立执行的代码2
    ......
elif 条件2：
  条件2成立执行的代码1
    条件2成立执行的代码2
    ......
......
else:
    以上条件都不成立执行执行的代码
```

多重判断也可以和else配合使用。一般else放在整个if语句的最后，表示以上条件都不成立的时候执行的代码。

> 思考：中国合法工作年龄为18-60岁，即如果年龄小于18的情况为童工，不合法；如果年龄在18-60岁之间为合法工龄；大于60岁为法定退休年龄。

#### 4.1 实例：工龄判断

```

age = int(input('请输入您的年龄：'))
if age < 18:
    print(f'您的年龄是{age},童工一枚')
elif (age >= 18) and (age <= 60):
    print(f'您的年龄是{age},合法工龄')
elif age > 60:
    print(f'您的年龄是{age},可以退休')
```

> 拓展：`age >= 18 and age <= 60`可以化简为`18 <= age <= 60`。

### 5. if嵌套

```
if 条件1：
  条件1成立执行的代码
    条件1成立执行的代码
    
    if 条件2：
      条件2成立执行的代码
        条件2成立执行的代码
```

注意：条件2的if也是出于条件1的缩进关系内部。

> 思考：坐公交：如果有钱可以上车，没钱不能上车；上车后如果有空座，则可以坐下；如果没空座，就要站着。怎么书写程序？

#### 5.1 实例：坐公交

1.判断是否能上车

```
"""
    1. 如果有钱，则可以上车
    2. 上车后，如果有空座，可以坐下
    上车后，如果没有空座，则站着等空座位
  如果没钱，不能上车
"""
# 假设用 money = 1 表示有钱, money = 0表示没有钱
money = 1
if money == 1:
    print('土豪，不差钱，顺利上车')
else:
    print('没钱，不能上车，追着公交车跑')
```

2. 判断是否能坐下

```
"""
  1. 如果有钱，则可以上车
    2. 上车后，如果有空座，可以坐下
    上车后，如果没有空座，则站着等空座位
  如果没钱，不能上车
"""
# 假设用 money = 1 表示有钱, money = 0表示没有钱; seat = 1 表示有空座，seat = 0 表示没有空座
money = 1
seat = 0
if money == 1:
    print('土豪，不差钱，顺利上车')
    if seat == 1:
        print('有空座，可以坐下')
    else:
        print('没有空座，站等')
else:
    print('没钱，不能上车，追着公交车跑')
```

#### 5.2 if嵌套执行流程

![image-20240628142032492](.\pic\第一天\if嵌套.png)

### 6. 练习：猜拳游戏

需求分析：

- 参与游戏的角色

- - 随机出拳
  - 手动出拳
  - 玩家
  - 电脑

- 判断输赢

  | 玩家 | 电脑 |
  | ---- | ---- |
  | 石头 | 剪刀 |
  | 剪刀 | 布   |
  | 布   | 石头 |

- - 玩家出拳 和 电脑出拳相同
  - 平局
  - 电脑获胜
  - 玩家获胜

随机做法：

   1.导出random模块

```
import 模块名
```

2. 使用random模块中的随机整数功能

```
random.randint(开始,结束)
```



### 7. 三目运算符

**三目运算符也叫三元运算符。**

语法如下：

```
值1 if 条件 else 值2
```

eg：

```
a = 1
b = 2

c = a if a > b else b
print(c)
```

## 十二、循环简介

### 1. 循环的作用

**让代码更高效的重复执行。**

### 2. 循环的分类

在Python中，循环分为`while`和`for`两种，最终实现效果相同。

### 3. while的语法

```
while 条件:
    条件成立重复执行的代码1
    条件成立重复执行的代码2
    ......
```

### 4. while循环快速体验

需求：复现重复执行10次`print('Hello World')`。

分析：初始值是0次，终点是10次，重复做的事情输出“Hello World”。

```
# 循环的计数器
i = 0
while i < 10:
    print('Hello World')
    i += 1

print('任务结束')
```

### 5. while的应用

#### 5.1 应用一：计算1-100累加和

分析：1-100的累加和，即1 + 2 + 3 + 4 +….，即前两个数字的相加结果 + 下一个数字( 前一个数字 + 1)。

```
i = 1
result = 0
while i <= 100:
    result += i
    i += 1

# 输出5050
print(result)
```

> 注意：为了验证程序的准确性，可以先改小数值，验证结果正确后，再改成1-100做累加。

#### 5.2 应用二：计算1-100偶数累加和

分析：1-100的偶数和，即 2 + 4 + 6 + 8…，得到偶数的方法如下：

- 偶数即是和2取余结果为0的数字，可以加入条件语句判断是否为偶数，为偶数则累加
- 初始值为0 / 2 , 计数器每次累加2





### 6. break和continue

**break和continue是循环中满足一定条件退出循环的两种不同方式。**

#### 6.1 理解

举例：一共吃5个苹果，吃完第一个，吃第二个…，这里"吃苹果"的动作是不是重复执行？

情况一：如果吃的过程中，吃完第三个吃饱了，则不需要再吃第4个和第五个苹果，即是吃苹果的动作停止，这里就是break控制循环流程，即终止此循环。

情况二：如果吃的过程中，吃到第三个吃出一个大虫子…,是不是这个苹果就不吃了，开始吃第四个苹果，这里就是continue控制循环流程，即退出当前一次循环继而执行下一次循环代码。

#### 6.2 break实例

```
i = 1
while i <= 5:
    if i == 4:
        print(f'吃饱了不吃了')
        break
    print(f'吃了第{i}个苹果')
    i += 1
```

![image-20240628142522419](.\pic\第一天\break.png)

#### 6.3 continue实例

```
i = 1
while i <= 5:
    if i == 3:
        print(f'大虫子，第{i}个不吃了')
        # 在continue之前一定要修改计数器，否则会陷入死循环
        i += 1
        continue
    print(f'吃了第{i}个苹果')
    i += 1
```

![image-20240628142608564](.\pic\第一天\continue.png)

### 7. while循环嵌套

#### 7.1 语法

```
while 条件1:
    条件1成立执行的代码
    ......
    while 条件2:
        条件2成立执行的代码
        ......
```

> 总结：所谓while循环嵌套，就是一个while里面嵌套一个while的写法，每个while和之前的基础语法是相同的。

#### 7.2 执行过程

当内部循环执行完成之后，再执行下一次外部循环的条件判断。
![image-20240628142653316](.\pic\第一天\循环.png)

#### 7.3 while循环嵌套应用

**应用一：打印星号（正方形）**

```
# 重复打印5行星星
j = 0
while j <= 4:
    # 一行星星的打印
    i = 0
    while i <= 4:
        # 一行内的星星不能换行，取消print默认结束符\n
        print('*', end='')
        i += 1
    # 每行结束要换行，这里借助一个空的print，利用print默认结束符换行
    print()
    j += 1
```

![image-20240628142815291](.\pic\第一天\打印星号.png)
**应用二：打印星号（三角形)**

```
# 重复打印5行星星
# j表示行号
j = 0
while j <= 4:
    # 一行星星的打印
    i = 0
    # i表示每行里面星星的个数，这个数字要和行号相等所以i要和j联动
    while i <= j:
        print('*', end='')
        i += 1
    print()
    j += 1
```

![image-20240628143105745](.\pic\第一天\打印三角形.png)
**练习：打印九九乘法表**

![image-20240628143022776](.\pic\第一天\九九乘法表.png)



![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

### 8. for循环

#### 8.1 语法

```
for 临时变量 in 序列:
    重复执行的代码1
    重复执行的代码2
    ......
```

#### 8.2 快速体验

```
str1 = 'Hello World'
for i in str1:
    print(i)
```

#### 8.3 break

```
str1 = 'Hello World'
for i in str1:
    if i == 'e':
        print('遇到e不打印')
        break
    print(i)
```

![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQFu6Mibzv7aXHcialDASRic6E8blDPh62RWCVZgbOLsuUbC0reTibRm2Uow/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

#### 8.4 continue

```
str1 = 'Hello World'
for i in str1:
    if i == 'e':
        print('遇到e不打印')
        continue
    print(i)
```

## 十三、else

循环可以和else配合使用，else下方缩进的代码指的是当循环正常结束之后要执行的代码。

### 1. while…else

#### 1.1 语法

```
while 条件:
    条件成立重复执行的代码
else:
    循环正常结束之后要执行的代码
```

#### 1.2 示例

```
i = 1
while i <= 5:
    print('Hello World')
    i += 1
else:
    print('执行完毕')
```

#### 1.3 退出循环的方式

1.break终止循环

```
i = 1
while i <= 5:
    if i == 3:
        print("提前结束")
        break
    print('Hello World')
    i += 1
else:
    print('执行完毕')
```

> 所谓else指的是循环正常结束之后要执行的代码，即如果是break终止循环的情况，else下方缩进的代码将不执行。

2.continue控制循环

```python
i = 1
while i <= 5:
    if i == 3:
        print("打断一下")
        i += 1
        continue
    print('Hello World')
    i += 1
else:
    print('执行完毕')![图片](https://mmbiz.qpic.cn/mmbiz_png/ULibHgXIt3jydv1F3CLdlHC9r4xClAHCQOcmnXTsDDpMKyb1HbpicGwlehM1HuR1kg6VniaoibS7VFS242ApEibhicKw/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)
```

> 因为continue是退出当前一次循环，继续下一次循环，所以该循环在continue控制下是可以正常结束的，当循环结束后，则执行了else缩进的代码。

### 2. for…else

#### 2.1 语法

```
for 临时变量 in 序列:
    重复执行的代码
    ...
else:
    循环正常结束之后要执行的代码
```

> 所谓else指的是循环正常结束之后要执行的代码，即如果是break终止循环的情况，else下方缩进的代码将不执行。

#### 2.2 示例

```
str1 = 'Hello World'
for i in str1:
    print(i)
else:
    print('循环正常结束之后执行的代码')
```

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate(-249.000000, -126.000000)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

#### 2.3 退出循环的方式

1.break终止循环

```
str1 = 'Hello World'
for i in str1:
    if i == 'e':
        print('遇到e不打印')
        break
    print(i)
else:
    print('循环正常结束之后执行的代码')
```

> 没有执行else缩进的代码。

2.continue控制循环

```
str1 = 'Hello World'
for i in str1:
    if i == 'e':
        print('遇到e不打印')
        continue
    print(i)
else:
    print('循环正常结束之后执行的代码')
```

> 因为continue是退出当前一次循环，继续下一次循环，所以该循环在continue控制下是可以正常结束的，当循环结束后，则执行了else缩进的代码。



课后练习：

##### ***\*任务1：从键盘接收一个整数\**** ***\*N\*******\*，统计出\**** ***\*1~N\**** ***\*之间能被\**** ***\*8\**** ***\*整除的整数的个数，以及这些能被\**** ***\*8\**** ***\*整除的数的和。\****

屏幕提示样例：

请输入一个整数：20

1~20 之间能被 8 整除的数的个数：2

1~20 之间能被 8 整除的所有数之和：24

要求：整数 N 由键盘输入，且 2 ≤ N ≤1000。

##### ***\*任务2：从键盘输入一个整数\**** ***\*N\*******\*，打印出有\**** ***\*N\*2-1\**** ***\*行的菱形。例如输入整数\**** ***\*4\*******\*，则屏幕输出如下菱形。\****

![img](.\pic\第一天\任务二.jpg) 

 

 

要求：①使用循环结构语句实现，直接输出不计分。②整数 N 由键盘输入， 且 2 ≤ N ≤10 。

##### 任务3：编程实现判断一个整数是否为素数。所谓素数是一个大于 1 的正整数，除了 1 和它本身，该数不能被其它的正整数整除。

