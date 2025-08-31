#  python语法

### 1.1.python的第一个程序

~~~python
print("Hello world!")
~~~

### 2.1.字面量

定义：在代码中，被写下来的固定的值.

**常用的值类型**

![image-20241009221030826](/images/image-20241009221030826.png)



### 2.2.注释

**注释**：在程序代码中对程序代码进行解释说明文字

> **作用**：注释不是程序，*不能被执行*，只是对程序代码进行解释说明，让别人更好的理解代码

分类：

1.单行注释：以“#”开头

~~~python
# 我是单行注释
print("hello,world")
~~~

2.多行注释：以一对三引号引起来（“”“注释内容”“”）

~~~python
"""
我是多行注释
第1行
第2行
第3行
"""
print("hello, world")
~~~



### 2.3.变量

> 变量：在程序运行时，能储存计算结果或能表示值的抽象概念。变量可以进行运算

~~~python
# 定义一个变量
money=20
print("钱包还有"，moeny)
~~~



### 2.4.数据类型

|  类型  |    描述    |                说明                 |
| :----: | :--------: | :---------------------------------: |
| string | 字符串类型 |    用引号引起来的数据都是字符串     |
|  int   |    整形    |  数字类型，存放整数，如-1，10，0等  |
| float  |   浮点型   | 数字类型，存放小数，如-3.14，6.66等 |

扩：

> type()语句

~~~python
print(type("666"))
print(type(666))
print(type(6.66))
~~~



### 2.5.数据类型的转换

|   语句   |      说明       |
| :------: | :-------------: |
|  int(x)  |  将x转换为整形  |
| float(x) | 将x转换为浮点型 |
|  str(x)  | 将x转换为字符串 |

~~~python
float_str=float("66.66")
~~~



### 2.6.标识符

> 标识符命名规则：
>
> 1.内容限定
>
> ​	英文，中文，数字，下划线
>
> ​	数字不允许在开头
>
> 2.不可以使用关键字
>
> 3.大小写敏感

> 命名规范：
>
> 1. 见命知意
> 2. 下划线命名法
> 3. 英文字母全小写     



### 2.7.运算符

![image-20241024192808788](../images/image-20241024192808788.png)

![image-20241024193432147](../images/image-20241024193432147.png)



### 2.8.字符串的扩展

> 1.定义方法

（1）.单引号定义法：name='super boy'

（2）.双引号定义法：name="super boy"

（3）.三引号定义法：name="""super boy"""

字符串引号的嵌套：

![image-20241024195251835](../images/image-20241024195251835.png)

> 2.字符串的拼接

两个字符串之间用“+”连接即可完成拼接

~~~python
name=小明
print("我是"+name)
~~~

> ###### 3.字符串的格式化

~~~python
name="小明"
age=18
print("我是%s今年%s"%(name,age))
~~~

* %表示：占位
* s表示：将变量变为字符串填入此处

![image-20241026193249601](../images/image-20241026193249601.png)

> 4.格式化的精度控制

**数字精度控制**

可以用辅助符号”m.n“控制数据的宽度和精度（”m“和”.n“均可省略）

* m控制宽度，设置的宽度小于数字自身，不生效
* n控制小数点精度，要求是数字，会进行小数的四舍五入

~~~python
num=11.45
#控制数字宽为5位，保留1位小数
print("%5.1f"%num)
~~~

> 5.字符串的格式化(2)

语法：f"内容{变量}"

~~~python
name="小明"
print(f"我是{name}")
~~~

> 6.对表达式进行格式化

表达式：具有明确执行结果的表达式

~~~python
print("1*1的结果是：%d"%(1*1))
print(f"1*2的结果是：{1*2}")
~~~



### 2.9.数据输入

> input语句

~~~python
name = input()
~~~

input的括号内可以直接填入提示内容

~~~python
name = input("你的名字是")
~~~

* input默认接受的数据类型是字符串。



### 3.1.布尔类型和比较运算符

**比较运算符**

![image-20241027183913640](../images/image-20241027183913640.png)

**布尔**

* Ture:表示为真
* Flase:表示为假

 

### 3.2.if语句的基本格式

~~~python
if 要判断的条件:
    条件成立时，执行的语句
~~~

例：

~~~python
age = 18
if age >= 18:
    print("已经成年")
~~~

判断结果为Ture,则执行语句,为Flase则跳过语句 。



### 3.3.if-else 语句

~~~python
if 条件:
    执行语句1
    执行语句2
    执行语句3
else:
    执行语句1
    执行语句2
    执行语句3
~~~

例：

~~~python
age = int(input("请输入你的年龄:"))
if age >= 18:
    print("你已成年")
else:
    print("你未成年")
~~~

### 3.4.if-elif-else语句

~~~python
if 条件:
    执行语句
elif 条件:
    执行语句
else:
    执行语句
~~~



### 4.1.循环语句

![image-20241112200244189](../images/image-20241112200244189.png)

### 4.2.while的循环语句

~~~python
while 条件:
	执行语句1
    执行语句2
    执行语句3
~~~

例:

~~~python
n=0
while n < 100:
    print(n)
    n += 1
~~~

**嵌套：**

~~~python
while 条件:
    执行语句1
    执行语句2
    执行语句3
    while 条件:
        执行语句1
        执行语句2
        执行语句3
~~~

### 补充（不换行）

~~~python
print("hello",end='')
# end='' 表示不换行
~~~



### 4.3.for 的循环语句

~~~python
for 临时变量 in 待处理数据集:
    循环语句
~~~

例：

~~~python
name="lihua"
for i in name:
    print(i)
~~~

* **range()语句**

![image-20241113201047152](../images/image-20241113201047152.png)

![image-20241113201056045](../images/image-20241113201056045.png)

![image-20241113201104868](../images/image-20241113201104868.png)

### 4.4.for循环的嵌套

![image-20241113202225307](../images/image-20241113202225307.png)

例：

~~~python
for i in range(1,10):
    for j in range(1:i):
        print(i*j)
~~~

### 4.5.循环的中端break和continue

* continue

![image-20241113202936517](../images/image-20241113202936517.png)

* break

![image-20241113203648033](../images/image-20241113203648033.png)



### 5.1.函数的介绍

函数：是组织好的，可重复使用的，用来实现特定功能的代码段

函数定义语法：

~~~python
def 函数名(传入参数):
    函数体
    return 返回值
~~~

函数的调用：

~~~python
函数名(参数)
~~~



### 5.2.函数的参数

例：

~~~python
def add(x,y):
    result = x + y
    print(result)
add(2,3)
// 输出结果为5
~~~



### 5.3.函数的返回值

函数运行后的结果

即 “return” 后的值或变量

可用变量接受返回值

返回值有none类型，即无返回值



### 5.4.函数的说明文档

例：

~~~python
def fun(x,y):
    """
    :param x:解释x
    :param y:解释y
    :return:返回值的说明
    """
    函数体
    return 返回值
~~~



### 5.5.函数的嵌套

函数的嵌套：在一个函数代码里有调用了另一个函数

例：

~~~python
def fun2():
    print("___2___")
def fun():
    print("___1___")
    fun2()
    print("___3___")
~~~



### 5.6.变量的作用域

作用域：变量的作用范围，主要分为局部变量和全局变量

* 全局变量：作用与整个python文件
* 局部变量：只作用于函数内部



### 6.1.数据容器

![image-20250224213517634](../images/image-20250224213517634.png)



### 6.2.List(列表)

##### 定义格式

~~~python
list = ["1","2","3"]
print(list)
~~~

![image-20250224213927271](../images/image-20250224213927271.png)

##### 下标索引

![image-20250224214716100](../images/image-20250224214716100.png)

![image-20250224214747234](../images/image-20250224214747234.png)

![image-20250224215009276](../images/image-20250224215009276.png)

##### 常用操作

![image-20250224215528848](../images/image-20250224215528848.png)

* index方法:查找元素的索引

例：

~~~python
list=["1","2","3"]
index =list.index("2")
~~~

* 修改元素

![image-20250224220044146](../images/image-20250224220044146.png)

* 插入元素![image-20250224220403452](../images/image-20250224220403452.png)

~~~python
list = ["1","2","4"]
list.insert(2,"3")
~~~

* 追加元素

![image-20250224220645452](../images/image-20250224220645452.png)

~~~python
list = ["1","2","3"]
list.append("4")
~~~

* 追加元素2

  ![image-20250224220837029](../images/image-20250224220837029.png)

~~~python
list = [1,2,3]
list.extend([4,5,6])
~~~

*  删除元素1

**方法一**

![image-20250224221057737](../images/image-20250224221057737.png)

~~~python
list = [1,2,3]
del list[0]
~~~

**方法二**

![image-20250224221243627](../images/image-20250224221243627.png)

~~~python
list = [1,2,3]
list.pop(1)
~~~

* 删除元素2

![image-20250224221513107](../images/image-20250224221513107.png)

~~~python
list = ["1","2","3","1"]
list.remove("1")
~~~

* 清空列表

![image-20250224221725669](../images/image-20250224221725669.png)

~~~python
list = ["1","2","3"]
list.clear()
~~~

* 统计某元素在列表中的数量

![image-20250224221845383](../images/image-20250224221845383.png)

* 统计列表中的元素数量

![image-20250224221957610](../images/image-20250224221957610.png)

~~~py
list = ["1","2","3"]
a = len(list)
~~~



总：![image-20250224222116851](../images/image-20250224222116851.png)



##### 遍历

![image-20250225122841287](../images/image-20250225122841287.png)

##### sort方法

![image-20250706152138423](../images/image-20250706152138423.png)

~~~py
my_list = [['a',33],['b',55],['c',11]]
def choose_sort_key(element):
    return element[1]

my_list.sort(key=choose_sort_key,reverse=True)
print(my_list)
~~~



### 6.2.Tuple(元组)

***元组的数据不可以修改***

![image-20250225123349633](../images/image-20250225123349633.png)

![image-20250225124811529](../images/image-20250225124811529.png)

* 元组的操作

![image-20250225213526754](../images/image-20250225213526754.png)



### 6.3.字符串

* 可以通过下标索引取值
* 字符串不支持修改
* index方法

~~~python
str = "hello,world"
a= str.index(5)
print(a)
~~~

* replace方法

![image-20250225214519561](../images/image-20250225214519561.png)

###### 1.字符串分割

* split用法

![image-20250225214819052](../images/image-20250225214819052.png)

注：是将字符串切分后存入列表中

###### 2.字符串规整操作

* strip()用法

![image-20250225215135978](../images/image-20250225215135978.png)

###### 3.统计字符串中出现某一字符出现的次数

* count用法

###### 4.求字符串的长度

* len()用法

##### 总结

![image-20250225215921928](../images/image-20250225215921928.png)



### 6.4.数据容器的切片

切片：从一个序列中，取出一个子序列

###### 语法：序列[起始下标:结束下标:步长]

![image-20250226180617923](../images/image-20250226180617923.png)

![image-20250226181347985](../images/image-20250226181347985.png)



### 6.5.集合

**不支持元素的重复**

![image-20250226181951698](../images/image-20250226181951698.png)

集合的元素是无序的，不支持下标索引

###### 操作

* 添加新元素

~~~py
myset={1,2,3,4,1,2}
myset.add(7)
~~~

* 移除元素

~~~py
myset={1,6,34,8,3,4,1}
myset.remove(1)
~~~

* 随机取出元素

~~~py
myset={1,4,55,6,1,3}
a=myset.pop()
~~~

随机取出一个元素，并且该元素会被从集合中移除

* 清空集合

~~~py
myset={1,5,3,6,8,9,25}
myset.clear()
~~~

* 取两个集合的差集

![image-20250226183003722](../images/image-20250226183003722.png)

* 消除两个集合的差集

![image-20250226183417912](../images/image-20250226183417912.png)

* 合并两个集合

![image-20250226183648683](../images/image-20250226183648683.png)

###### 集合的遍历

集合不支持while循环遍历，但支持for循环遍历



###### 总结

![image-20250226184417984](../images/image-20250226184417984.png)



### 6.6.字典

###### 字典的定义

  ![image-20250226190909946](../images/image-20250226190909946.png)

字典的key不允许重复

字典是可以嵌套的

###### 字典操作

* 新增元素

![image-20250226192611245](../images/image-20250226192611245.png)

* 更新元素

![image-20250226192640520](../images/image-20250226192640520.png)

* 删除元素

~~~py
//删除元素
my_dict={
    1:6,2:7,3:8
}
score = my_dict.pop(1)
~~~

* 得到字典的全部key

  可以用于字典的遍历

~~~py
my_dict={
    1:6,2:7,3:8
}
score = my_dict.keys()
~~~

* 字典的遍历

字典不支持while循环遍历

只支持for循环遍历

* 统计字典元素的数量len()

###### 总结

![image-20250226193650766](../images/image-20250226193650766.png)



### 6.7.数据容器的通用操作

![image-20250226194510061](../images/image-20250226194510061.png)

![image-20250226195835233](../images/image-20250226195835233.png)

![image-20250226200502139](../images/image-20250226200502139.png)

~~~py
list=[1,2,5,7,9,6,22,1,3]
new_list=sorted(list)
//从大到小排序
//当sorted()函数中有[reverse=True]时，是将数据容器反序排序
~~~



### 7.1.函数的多返回值

![image-20250226201522648](../images/image-20250226201522648.png)

![image-20250226201613938](../images/image-20250226201613938.png)



### 7.2.函数的多种传参方式

* 位置参数

![image-20250226202334506](../images/image-20250226202334506.png)

* 关键字参数

![image-20250226202554471](../images/image-20250226202554471.png)

* 不定长参数

![image-20250226203319509](../images/image-20250226203319509.png)

![image-20250226203539170](../images/image-20250226203539170.png)

![image-20250226203750862](../images/image-20250226203750862.png)

* 缺省参数

![image-20250226204328291](../images/image-20250226204328291.png)



### 7.3.匿名函数

函数可以作为参数被另一个函数接受

![image-20250226204803824](../images/image-20250226204803824.png)

###### lambda匿名函数

![image-20250226205829549](../images/image-20250226205829549.png)

~~~py
def func(x,y):
    return x+y

lambda x,y : x+y

//两者功能相同
~~~



### 7.4.递归

![image-20250226210457683](../images/image-20250226210457683.png)



### 8.1.文件的编码

计算机中有很多的可用编码

* UTF-8
* GBK
* BIG5

电脑一般使用UTF-8

### 8..2.文件的读取操作

* open()函数

![image-20250226211600590](../images/image-20250226211600590.png)

![image-20250226211816022](../images/image-20250226211816022.png)

* 读操作的相关方法

![image-20250226212151490](../images/image-20250226212151490.png)

readline()方法：

一次读取一行，读取类型为字符串

* 关闭文件对象

close()函数

~~~py
f.close()
~~~

* with open()读取文件

![image-20250226214417340](../images/image-20250226214417340.png)

### 8.3.文件的写出操作

* write()写入

~~~py
f = open("test.txt",'a',encoding="UTF-8")
f.write("hello,world")
f.flush()
// write()并不是将内容写入文件，而是写入缓存中
//flush()方法执行后才写入文件中
//close()方法内置flush()功能
~~~

![image-20250226220317518](../images/image-20250226220317518.png)

### 8.4.文件的追加操作

![image-20250226220422884](../images/image-20250226220422884.png)

将w模式替换为a模式



### 9.1.了解异常

当程序出现异常时，会出现一些错误的提示，称为“异常”。

bug就是异常的意思



### 9.2.异常的捕获

~~~py
try:
    可能发生错误的代码
except:
    出现异常后执行的代码
~~~



例子：

~~~py
try:
    f = open("text.txt",'r',encoding='utf-8')
except:
    print("出现异常，文件不存在，将open的模式改为w")
	f = open('text.txt','w',encoding='utf-8')

# 捕获特定的异常
# 只会捕获NameError类型的bug
try :
    print(name)
except NameError as e:
    print(e)
    
# 捕获多个异常
try:
    1/0
except (NameError, ZeroDivisionError) as e:
    print(e)
    
# 捕获所有的异常
try:
    f = open("text.txt",'r',encoding='utf-8')
# Exception表示会捕获所有的异常
except Exception as e:
    print(e)
    f = open('text.txt','w',encoding='utf-8')
else:
    print("无异常")
finally:	# 无论有无异常，finally下的语句都会执行
    f.close()
~~~



### 9.3.异常的传递

异常具有传递性

~~~py
# 演示异常的传递性

# （1）定义一个出现异常的方法
def func01():
    print("func01开始执行")
    num = 1/0
    print("func01执行结束")

# （2）定义一个无异常的方法，调用上面的方法
def func02():
    print("func02开始执行")
    func01()
    print("func02执行结束")

# （3）定义一个无异常方法，调用上面方法
def func03():
    try:
        func02()
    except ZeroDivisionError as e:
        print(e)

func03()
~~~



### 9.4.Python模块的概念和导入

模块就是一个python文件，用来实现一些功能

~~~py
# 语法：
[from 模块名] import [模块|类|变量|函数|*] [as 别名]

# 常用的组合形式：
import 模块名
from 模块名 import 类、变量、方法等
from 模块名 import *
import 模块名 as 别名
from 模块名 import 功能名 as 别名
~~~

~~~py
# 使用import导入time模块使用sleep()功能
import time
time.sleep(2)

# 使用from导入time的sleep()功能
from time import sleep
time.sleep(5)

# 使用*导入time的所有功能
from time import *		# *表示全部
time.sleep(5)

# 使用as给特定的功能加上别名
import time.sleep as s
s(1)

~~~



### 9.5.自定义模块

新建一个py文件，就可以作为模块

~~~py
# 模块文件	文件名称为：my_module.py
def add(a,b):
    return a+b
def minus(a,b):
    return a-b
~~~

~~~py
import my_module
a = 5
b = 3
c = my_module.add(a,b)
print(c)
~~~

注：当导入两个模块时，且两个模块有相同的函数名时，会执行后导入的模块的函数



~~~py
if __name__=='__main__':
~~~

语句可以再文件内部导入时可以运行其内部的语句，当被外部测试时则不会执行其内部的代码



~~~py
__all__=['add']
# 当使用form my_module improt * 时只能导入add函数
~~~



### 9.6.Python包

#### (1.)自定义一个包

python包就是一个文件夹，并且该文件夹下包含了一个‘’**__init__**.py‘’文件

~~~py
同时 __all__=[]语句要写入__init__.py文件下
~~~



![image-20250522192539830](../images/image-20250522192539830.png)

~~~py
# my_module_1
def info_print1():
    print("模块1")
~~~

~~~py
# my_module_2
def info_print2():
    print("模块2")
~~~

~~~py
# 主文件
import my_pakeage.my_module_1
import my_pakeage.my_module_2
my_pakeage.my_module_1.info_print1()
my_pakeage.my_module_2.info_print2()
~~~



#### (2.)安装第三方包

在命令提示符中输入 

  ~~~py
  pip install 包名称
  ~~~

~~~py
# 使用清华的镜像网站下载包
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple 包名称
~~~



### 10.1.Json数据格式的转换

##### （1）json定义

json是一种轻量级的数据交互格式。可以按照json指定的格式去组织和封装数据

json本质上是一个带有特定格式的字符串

主要功能：json就是一种在各个编程语言中流通的数据格式，负责不同编程语言中的数据传递和交互。

##### （2）json格式数据转化

~~~json
# 第一种格式
{"name":"admin","age":"18"}
~~~

~~~json
# 第二种格式
[{"name":"admin","age":"18"},{"name":"root","age":"16"},{"name":"张三","age":"20"}]
~~~



~~~python
import json
# 准备符合json格式要求的python数据
data=[{"name":"admin","age":"18"},{"name":"root","age":"16"}]
# 通过json.dumps(data)方法把python数据转化为json数据
data = json.dumps(data)
# 通过json.loads(data)方法把json数据转化为python数据
data = json.loads(data)
~~~

~~~py
### 示例
import json
data=[{"name":"admin","age":"18"},{"name":"张三","age":"16"}]
# 通过json.dumps(data)方法把python数据转化为json数据
# 可以使中文正常输出
data = json.dumps(data,ensure_ascii=False)
print(data)
# 通过json.loads(data)方法把json数据转化为python数据
data = json.loads(data)
print(data)
~~~



### 10.2.pyecharts模块

可以通过(https://gallery.pyecharts.org/#/)查看pyecharts的信息和作用

~~~py
# 生成折线图

from pyecharts.charts import Line

# 得到直线图对象
line = Line()
# 添加X轴数据
line.add_xaxis([1,2,3,4,5,6,7,8,9,10])
# 添加y轴数据
line.add_yaxis("number",[1,2,3,4,5,6,7,8,9,10])
# 生成图像
line.render()

~~~

~~~py
# set_global_opts方法
# 设置全局配置
line.set_global_opts(
    # 标题设置
    title_opts = TitleOpts(title='Number',pos_left='center',pos_bottom='20px',pos_right='20px',pos_top='20px'),
    # title 是标题     pos_left 是标题距离左边框的位置    pos_bottom,pos_top,pos_right同理

    # 图例设置
    legend_opts = LegendOpts(is_show=True),

    # 工具箱设置
    toolbox_opts = ToolboxOpts(is_show=True),

)
# 生成图像
line.render()
~~~



懒人工具网站：[懒人工具-json在线解析-在线JSON格式化工具-json校验-程序员必备](http://www.kuquidc.com/)



### 11.1.基础地图可视化

~~~py
from pyecharts.charts import Map
from pyecharts.options import VisualMapOpts

# 添加地图对象
map = Map()
# 准备数据
data = [
    ("北京市", 99),
    ("上海市", 199),
    ("湖南省", 299),
    ("台湾省", 399),
    ("广东省", 499)
]
# 添加数据
map.add("测试地图",data,"china")
# 设置全局选项
map.set_global_opts(
    visualmap_opts=VisualMapOpts(
        is_show=True,
        is_piecewise=True,
        pieces=[
            {"min": 1, "max": 99,"label":"1-99","color":"#CCFFFF"},
            {"min": 100, "max": 199,"label":"100-199","color":"#000012"},
            {"min": 200, "max": 299,"label":"200-299","color":"#001234"},
            {"min": 201, "label":"201以上","color":"#000012"},
        ],
    )
)
# 绘制地图
map.render()

~~~



### 12.1.柱状图

#### 1.基础柱状图

~~~py
from pyecharts.charts import Bar
from pyecharts.options import LabelOpts
# 使用Bar构建基础柱状图
bar = Bar()
# 添加x轴数据
bar.add_xaxis(["中国","美国","英国"])
# 添加y轴数据，将数据标签放在右边
bar.add_yaxis("GDP",[100,50,30],label_opts=LabelOpts(position="right"))
# 反转x,y轴
bar.reversal_axis()
# 绘图
bar.render("柱状图.html")


~~~

#### 2. 动态柱状图

~~~py
# 创建时间线
from pyecharts.charts import Bar,Timeline
from pyecharts.options import *
from pyecharts.globals import ThemeType

bar1 = Bar()
bar1.add_xaxis(["中国","美国","英国"])
bar1.add_yaxis("GDP",[100,50,30],label_opts=LabelOpts(position="right"))

bar2 = Bar()
bar2.add_xaxis(["中国","美国","英国"])
bar2.add_yaxis("GDP",[120,55,40],label_opts=LabelOpts(position="right"))

bar3 = Bar()
bar3.add_xaxis(["中国","美国","英国"])
bar3.add_yaxis("GDP",[90,45,20],label_opts=LabelOpts(position="right"))

# 构建时间线对象
timeline = Timeline(
    {"theme":ThemeType.LIGHT}
)
# 在时间线内添加柱状图对象
timeline.add(bar1,"001")
timeline.add(bar2,"002")
timeline.add(bar3,"003")
# 自动播放设置
timeline.add_schema(
    is_auto_play=True,
    play_interval=1000,
    is_timeline_show=True,
    is_loop_play=True
)
# 绘图时用时间线绘图
timeline.render("timeline.html")

~~~



### 13.1.初始对象

![image-20250706194341116](../images/image-20250706194341116.png)

~~~py
# 设计一个类
class student:
    name = None     # 姓名
    sex = None  # 性别
    age = None   # 年龄
    nationality = None      # 学生国籍
    native_place = None     # 学生籍贯

# 创建一个对象
stu1 = student()

# 对对象属性进行赋值
stu1.name = "凌俊杰"
stu1.sex = "男"
stu1.age = 18
stu1.nationality = "中国"
stu1.native_place = "山东"

# 输出对象中记录的信息
print(stu1.name)
print(stu1.sex)
print(stu1.age)
print(stu1.nationality)
print(stu1.native_place)
~~~



### 13.2.类的成员方法

![image-20250706194944734](../images/image-20250706194944734.png)

![image-20250706195249239](../images/image-20250706195249239.png)

~~~python
# 设计一个类
class student:
    name = None     # 姓名

    def say_hi(self):
        print(f'大家好，我是{self.name}')

    def say_hello(self,msg):
        print(f"大家好,{msg}，{self.name}")

# 创建一个对象
stu1 = student()
stu2 = student()
stu3 = student()

# 对对象属性进行赋值
stu1.name = "凌俊杰"
stu2.name = "张俊杰"
stu3.name = "周俊杰"

# 输出对象中记录的信息
stu1.say_hi()
stu2.say_hi()
stu3.say_hi()
stu1.say_hello("我是练习时长两年半的练习生")
~~~



### 13.3.类和对象

![image-20250707150249910](../images/image-20250707150249910.png)

~~~py
# 设计一个闹钟类
class clock:
    id = None   # 序列化
    price = None    #价格

    def ring(self):
        import winsound
        winsound.Beep(1000,500)

# 构建2个闹钟对象，并进行工作
clock1 = clock()
clock2 = clock()
clock1.ring()
clock2.ring()
~~~



### 13.4.构造方法

![image-20250707151507582](../images/image-20250707151507582.png)

~~~py
class Student:
    name = None
    age = None
    tel = None

    def __init__(self, name, age, tel):
        self.name = name
        self.age = age
        self.tel = tel
        print("Student创建了一个类对象")


stu1 = Student("凌俊杰", 18, "1589642666")
print(stu1.name)
print(stu1.age)
print(stu1.tel)
~~~



### 13.5.类内置方法

#### 1.字符串方法

~~~py
class Student:
    name = None
    age = None

    def __init__(self, name1, age1, ):
        self.name = name1
        self.age = age1

    def __str__(self):
        return f'Student类对象：name:{self.name} ,age:{self.age}'

stu = Student("凌俊杰", 20)
print(stu)
print(str(stu))
~~~



#### 2.小于符号比较方法

~~~py
class Student:
    name = None
    age = None

    def __init__(self, name1, age1, ):
        self.name = name1
        self.age = age1
	
    # 小于
    def __lt__(self, other):
        return self.age < other.age


stu2 = Student("周杰伦", 22)
stu = Student("凌俊杰", 20)

print(stu > stu2)
~~~



#### 3.小于等于比较方法

~~~py
class Student:
    name = None
    age = None

    def __init__(self, name1, age1, ):
        self.name = name1
        self.age = age1

    # 小于等于
    def __le__(self, other):
        return self.age =< other.age


stu2 = Student("周杰伦", 22)
stu = Student("凌俊杰", 20)

print(stu >= stu2)

~~~



#### 4.相等比较方法

~~~py
class Student:
    name = None
    age = None

    def __init__(self, name1, age1, ):
        self.name = name1
        self.age = age1

    def __eq__(self, other):
        return self.age == other.age


stu2 = Student("周杰伦", 22)
stu = Student("凌俊杰", 20)

print(stu == stu2)

~~~



### 13.6.封装

![image-20250707190520966](../images/image-20250707190520966.png)

私有变量无法赋值，也无法获取

私有成员函数无法直接被类对象调用

~~~py
class Phone:
    __current_voltage = None    # 当前手机运行电压

    def __keep_single_score(self):
        print("让CPU以单核模式运行")


phone = Phone()
phone.__current_voltage = 3.3
phone.__keep_single_score
~~~

~~~py
运行结果：
Traceback (most recent call last):
  File "D:\code\python\pythonProject1\对象.py", line 10, in <module>
    phone.__keep_single_score
AttributeError: 'Phone' object has no attribute '__keep_single_score'. Did you mean: '_Phone__keep_single_score'?

~~~

**私有成员无法被类对象使用，但可以被其他的成员使用**

~~~py
class Phone:
    __current_voltage = 1    # 当前手机运行电压

    def __keep_single_score(self):
        print("让CPU以单核模式运行")

    def call_by_5g(self):
        if self.__current_voltage >= 1:
            print("5g通话已开启")
        else:
            print("电量不足，无法使用5g通话")


phone = Phone()
phone.call_by_5g()
~~~

~~~py
运行结果：
5g通话已开启
~~~



### 13.7.继承的基础语法

* 单继承：一个子类继承了一个父类

  ![image-20250707194004674](../images/image-20250707194004674.png)

~~~py
class Phone:
    IMEI = None     #序列号
    producer = "HM" #厂商

    def call_by_4g(self):
        print("4g通话")


class Phone2022(Phone):
    IMEI = "2022"
    face_id = "10001"   # 面部识别

    def call_by_5g(self):
        print("2022年新功能：5G通话")


phone2022 = Phone2022()
print(Phone2022.producer)
phone2022.call_by_4g()
phone2022.call_by_5g()
~~~



* 多继承：

  ![image-20250707194608264](../images/image-20250707194608264.png)

~~~py
# 手机类
class Phone:
    IMEI = None         # 序列号
    producer = "HM"     # 厂商

    def call_by_4g(self):
        print("4g通话")


class Phone2022(Phone):
    IMEI = "2022"
    face_id = "10001"   # 面部识别

    def call_by_5g(self):
        print("2022年新功能：5G通话")

# NFC读卡器类
class NFC_Reader:
    nfc_type = "第五代"
    producer = "HM"

    def read_card(self):
        print("NFC读卡")

    def write_card(self):
        print("NFC写卡")

# 红外遥控器类
class RemoteControl:
    rc_type = "红外遥控"

    def control(self):
        print("红外遥控开启了")

class my_phone(Phone2022, NFC_Reader, RemoteControl):
    pass


my_phone().read_card()
my_phone().write_card()
my_phone().call_by_4g()
~~~

![image-20250707195748835](../images/image-20250707195748835.png)



### 13.8.复写父类成员和调用父类成员

复写：在子类中重新定义同名的属性或方法

~~~py
# 手机类
class Phone:
    IMEI = None         # 序列号
    producer = "HM"     # 厂商

    def call_by_5g(self):
        print("5g通话")


class my_phone(Phone):
    producer = "ITCAST"

    def call_by_5g(self):
        print("开启CPU单核模式")
        print("使用5g通话")


phone = my_phone()
print(phone.producer)
phone.call_by_5g()
~~~



调用父类成员:

![image-20250708150832722](../images/image-20250708150832722.png)

~~~py
# 手机类
class Phone:
    IMEI = None         # 序列号
    producer = "HM"     # 厂商

    def call_by_5g(self):
        print("5g通话")


class my_phone(Phone):
    producer = "ITCAST"

    def call_by_5g(self):
        print("开启CPU单核模式")
        print("使用5g通话")
        Phone.call_by_5g(self)
        print(f"父类的厂商是{Phone.producer}")


phone = my_phone()
print(phone.producer)
phone.call_by_5g()
~~~

~~~py
# 手机类
class Phone:
    IMEI = None         # 序列号
    producer = "HM"     # 厂商

    def call_by_5g(self):
        print("5g通话")


class my_phone(Phone):
    producer = "ITCAST"

    def call_by_5g(self):
        print("开启CPU单核模式")
        print(f"父类的厂商是：{super().producer}")
        super().call_by_5g()

phone = my_phone()
print(phone.producer)
phone.call_by_5g()
~~~



### 13.9.类型注解

 ![image-20250708152522823](../images/image-20250708152522823.png)

![image-20250708152639589](../images/image-20250708152639589.png)

~~~ py
var_1: int = 10
var_2: float = 3.1415926
var_3: bool = True
~~~

~~~py
class Student:
    name = None
    
    def __init__(self,Name):
        name = Name
        

stu: Student = Student()
~~~

![image-20250708152917846](../images/image-20250708152917846.png)

![image-20250710152455157](../images/image-20250710152455157.png)



### 13.10.函数和方法的类型注解

![image-20250710153450693](../images/image-20250710153450693.png)

~~~py
def add(x: int, y: int) -> int:
    return x + y


def subtract(x: int, y: int) -> int:
    return x - y
~~~



### 13.11.Union类型

![image-20250710154254150](../images/image-20250710154254150.png)

![image-20250710154341093](../images/image-20250710154341093.png)

~~~py
from typing import Union
my_list: list[Union[int, str]] = [1, 2, "123", 3]


def func(data: Union[int, str]) -> Union[int, str]:
    pass
~~~



### 13.12.多态

**多态：指的是多种状态，即完成某个行为时，使用不同的对象会得到不同的状态**

![image-20250710155218802](../images/image-20250710155218802.png)

 ~~~py
 class Animal:
     def speak(self):
         pass
 
 
 class Dog(Animal):
     def speak(self):
         print("woof woof woof woof woof")
         pass
 
 
 class Cat(Animal):
     def speak(self):
         print("miao miao miao miao miao")
 
 
 def make_noise(animal: Animal):
     animal.speak()
     pass
 
 
 dog = Dog()
 cat = Cat()
 make_noise(dog)
 make_noise(cat)
 ~~~

![image-20250710160127750](../images/image-20250710160127750.png)



### 14.1.My SQL基本使用

~~~sql
mysql -uroot -p
~~~

进入My SQL

![image-20250717234404379](../images/image-20250717234404379.png)

![image-20250717234521726](../images/image-20250717234521726.png)



### 14.2.SQL基础和DDL

![image-20250719193933941](../images/image-20250719193933941.png)

1..SQL语句大小写不敏感

2.SQL可以单行或多行书写，最后以“;”结尾

3.SQL支持注释：

* 单行注释： -- *注释内容*（--后面有一个空格）
* 单行注释：# *注释内容*（#后面可以不加空格，推荐加上）
* 多行注释：/**注释内容* */



#### 1.库管理

~~~sql
# 查看数据库
show databases;
~~~

~~~sql
# 使用数据库
use 数据库名称;
~~~

~~~sql
# 创建数据库
create database 数据库名称 [charset utf8];
~~~

~~~sql
# 删除数据库
drop database 数据库名称;
~~~

~~~sql
# 查看当前使用的数据库
select database();
~~~



#### 2.表管理

~~~sql
# 查看有哪些表
show tables;
~~~

~~~sql
# 删除表
drop table 表名称;
drop table if exists 表名称;
~~~

~~~sql
# 创建表
create table 表名称(
	列名称 列类型,
    列名称 列类型,
    列名称 列类型,
    ......
)
~~~

![image-20250719201103433](../images/image-20250719201103433.png)



### 14.3.SQL ---  DML

* 插入数据insert

~~~sql
-- 基础语法
insert into 表[(列1, 列2, ...... 列n)] values(值1, 值2， ......值n)[,(值1, 值2， ......值n), .......(值1, 值2， ......值n)]
~~~

~~~sql
-- 例：
create table student(
	id int, -- 学号
	name varchar(10), -- 姓名
	age int -- 年龄
);

insert into student(id, name, age) values(1, '周杰伦', 31),
(2, '林俊杰', 32),(3, '刘德华', 34);
~~~



* 删除数据delete

~~~sql
-- 基础语法
delete from 表名称 [where 条件判断]
~~~

![image-20250719214402320](../images/image-20250719214402320.png)

~~~sql
-- 例：
use world;
delete from student where id = 1;
~~~



* 数据更新update

~~~sql
-- 基础语法
update 表名 set 列=值 [where 条件判断];
~~~

~~~sql
-- 例：
use world;
update student set age = 29 where name='林俊杰';
~~~



### 14.4.SQL --- DQL

![image-20250721174743754](../images/image-20250721174743754.png)

#### 1.基础查询

~~~sql
-- 基础语法
select 字段列表|* from 表
~~~

~~~sql
-- 例：
select * from student;
~~~

~~~sql
-- 例：
select * from student where age > 31;
~~~



#### 2.分组聚合

一个SQL语句中可以有多个聚合函数

~~~sql
-- 基础语法
select 字段|聚合函数 from 表 [where 条件] group by 列
~~~

![image-20250721173609158](../images/image-20250721173609158.png)

~~~sql
-- 例：
select age,count(name) as 人数 from student group by student.age;
~~~



#### 3.排序分页

可以对查询结果，使用order by 关键字，指定某个列进行排序。

~~~sql
-- 基础语法
select 列|聚合函数|* from 表
where ...
group by ...
order by ... [asc|desc];

-- asc 表示升序，默认为升序
-- desc 表示降序
~~~

~~~sql
-- 例：
select * from student where age > 20 order by age asc;
~~~



可以使用LIMIT关键字，对查询结果进行数量限制或分页查询

~~~sql
-- 基础语法
select 列|聚合函数|* from 表
where ...
group by ...
order by ...[asc|desc]
limit n[,m]
-- n 表示显示几行
-- m 表示第n行后取几行
~~~

~~~sql
-- 例：
select * from student where age > 20 order by age asc limit 10,5;
~~~



### 14.5.Python和SQL的基础使用

需要前置库：pymysql 和 cryptography

~~~~py
from pymysql.connections import Connection
# 获取到MySQL数据库的连接对象
conn = Connection(
    host='localhost',   # 主机名（或IP地址）
    user='root',        # 账户名
    password='575784620.',    # 密码
    port=3306,          # 端口，默认3306
)

# 打印MySQL数据库软件信息
print(conn.get_server_info())
# 关闭到数据库的链接
conn.close()

~~~~



执行非查询性质的SQL语句

~~~py
from pymysql.connections import Connection
# 获取到MySQL数据库的连接对象
conn = Connection(
    host='localhost',   # 主机名（或IP地址）
    user='root',        # 账户名
    password='575784620.',    # 密码
    port=3306,          # 端口，默认3306
)

# 获取游标对象
cursor = conn.cursor()
conn.select_db('test')      # 选择数据库
# 使用游标对象，执行SQL语句
cursor.execute("create table test_pymysql(id int, name varchar(20))")

# 关闭到数据库的链接
conn.close()
~~~



执行查询性质的SQL语句

~~~py
from pymysql.connections import Connection
# 获取到MySQL数据库的连接对象
conn = Connection(
    host='localhost',   # 主机名（或IP地址）
    user='root',        # 账户名
    password='575784620.',    # 密码
    port=3306,          # 端口，默认3306
)

# 获取游标对象
cursor = conn.cursor()
conn.select_db('test')      # 选择数据库
# 使用游标对象，执行SQL语句
cursor.execute("select * from student")
# 获取查询结果
result: tuple = cursor.fetchall()
for i in result:
    print(i)
# 关闭到数据库的链接
conn.close()
~~~



执行插入的SQL语句

需要用到commit语句，否则不会向数据库插入元素

~~~py
from pymysql.connections import Connection
# 获取到MySQL数据库的连接对象
conn = Connection(
    host='localhost',   # 主机名（或IP地址）
    user='root',        # 账户名
    password='575784620.',    # 密码
    port=3306,          # 端口，默认3306
)

# 获取游标对象
cursor = conn.cursor()
conn.select_db('test')      # 选择数据库
# 使用游标对象，执行SQL语句
cursor.execute("insert into student values (10021, '刘亦菲', 34, '女')")
conn.commit()
# 关闭到数据库的链接
conn.close()

~~~

也可设置自动执行commit语句

~~~py
from pymysql.connections import Connection
# 获取到MySQL数据库的连接对象
conn = Connection(
    host='localhost',   # 主机名（或IP地址）
    user='root',        # 账户名
    password='575784620.',    # 密码
    port=3306,          # 端口，默认3306
    autocommit=True     # 自动执行commit语句
)

# 获取游标对象
cursor = conn.cursor()
conn.select_db('test')      # 选择数据库
# 使用游标对象，执行SQL语句
cursor.execute("insert into student values (10021, '刘亦菲', 34, '女')")
# 关闭到数据库的链接
conn.close()

~~~



示例：

~~~py
from pymysql import Connection
import json
from typing import Union
def read_txt(path) -> list[Union[str, int]]:
    data_list = []
    f = open(path, 'r', encoding='utf-8')
    lines = f.readlines()
    for line in lines:
        line = line.strip()
        data = line.split(',')
        data_list.append(data)

    return data_list



conn = Connection(
            host="localhost",
            port=3306,
            user="root",
            password="575784620.",
        )
cursor = conn.cursor()
conn.select_db('test')
data = read_txt('2011年1月销售数据.txt')
cursor.execute("create table test_sale(日期 datetime, 订单号 varchar(80), 销量 int, 省份 varchar(10))")

for line in data:
    sql = "insert into test_sale values(%s,%s,%s,%s)"
    cursor.execute(sql, (line[0], line[1], line[2], line[3]))

conn.commit()
conn.close()

if __name__ == '__main__':
    print(read_txt("2011年1月销售数据.txt"))

~~~

~~~py
from pymysql import Connection
import json
from typing import Union
def read_json(path) -> list[Union[str, int]]:
    data_list = []
    f = open(path, 'r', encoding='utf-8')
    lines = f.readlines()
    for line in lines:
        data_josn = json.loads(line)
        data_list.append(data_josn)

    return data_list



conn = Connection(
            host="localhost",
            port=3306,
            user="root",
            password="575784620.",
        )
cursor = conn.cursor()
conn.select_db('test')
data = read_json('2011年2月销售数据JSON.txt')
cursor.execute("create table test_sale_json(日期 datetime, 订单号 varchar(80), 销量 int, 省份 varchar(10))")

for line in data:
    sql = "insert into test_sale_json values(%s,%s,%s,%s)"
    cursor.execute(sql, (line['date'], line["order_id"], line['money'], line['province']))



conn.commit()
conn.close()

if __name__ == '__main__':

    print(read_json("2011年2月销售数据JSON.txt")[0]['date'])

~~~



### 15.1.PySpark基础

定义：Apache Spark是用于大规模数据处理的统一分析

构建PySpark执行环境入口对象

~~~py
~~~


