## 开始第一个程序

### 使用Python **.py 与直接执行 **.py区别

直接输入python,相当于进入到python解释器中，当你一行一行输入代码，就会一行一行的执行代码

直接运行.py文件，相当于启动了Python解释器，然后把`.py`文件中的源代码一次性执行了

#### 编写直接运行的py文件

1. 文件首行配置执行环境

   ``` #! /usr/bin/env python3 ```

2. 配置文件可执行

   ``` chmod +x hello.py ```

## 数据类型

### 基础数据类型

1. 整数
2. 浮点数
3. 字符串
4. 布尔值
5. 空值 : None

### dict-(dictionary)

```python
>>> d = {'Michael': 95, 'Bob': 75, 'Tracy': 85}
>>> d['Michael']
95
```

元素操作：

```python
d.pop("Bob") // 删除"Bob"对象
d.['Jack'] = 80 //增加'Jack'对象
```

### set

特点：集合内数据，没有重复的key

```python
>>> s = set([1,2,3,4,2,1,2])
>>> s
{1, 2, 3, 4}
```

### list

Python内置的一种数据结构，list是一种有序的集合，可以随时删除和新增数据。

```python
# 定义list，使用[]
visitors = ['Jack','Rose']
# 获取list长度
len(visitors)
# 访问元素
visitors[1]
# 向有序列表队尾添加元素
visitors.append('Chen')
# 向有序队列的指定位置添加元素
visitors.insert(1,'Lin')
# 删除队尾元素
visitors.pop()
# 删除指定位置元素
visitors.pop(i)
# 队列数据替换
visitors[1] = 'Sarah'

```

### tuple

与list类似，但是tuple一经初始化后，便不能修改

```python
# 初始化tuple
visitors = ('Jack','Rose')
# 定义单独数据,使用逗号分隔，否则会忽略tuple初始化，看成普通括号
visitor = (1,)
```



## 条件判断

### if/elif/else

```python
age = 3
if age >= 18:
    print('adult')
elif age >= 6:
    print('teenager')
else:
    print('kid')
```



注意格式说明，条件判断之后需要使用":"，注意条件关键字，注意缩进

### 循环

#### for...in

```python
for x in [1,2,3]
	print(x)
```

#### while

```python
sum = 0
n = 99
while n>0:
	sum = sum + n
	n = n-2
print(n)	
```

#### break/continue

在循环中，break语句可以跳出循环

在循环中，continue可以跳出这次循环，直接开始下一次循环

## 函数

### python内置函数

直接使用,不需要显示调用,例如`abs` `max`

### 定义方法

#### 常规模式

```python
def my_abs(x):
  if(x>=0):
    return x
  else:
    return -x
```

#### 空函数

```python
def nop():
	pass
```

#### 参数检查

```python
def my_abs(x):
  if not isinstance(x,(int,float)):
    raise TypeError('bad operand type')
  if(x>=0):
    return x
  else:
    return -x
```

返回多个值

