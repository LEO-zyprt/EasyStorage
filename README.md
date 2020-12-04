# EasyStorage

chr(66) # number to character
ord('string') # character to number

x = b'ABC'
'ABC'.encode('ascii')
'中文'.encode('utf-8')  #汉字没有ascii

b'ABC'.decode('utf-8') # get ABC
b'\xe4\xb8\xad\xff'.decode('utf-8', errors = 'ignore')

#!/usr/bin/env python3
#-*- coding: utf-8 -*-  当源代码存在中文的时候

# 格式化 %f:float %x:十六进制
'Hi, %s, you have $%d.' % ('Michael', 1000000)
'%d-%02d' % (3, 1) #2是为了空出位，0是为了用0补位
'%.2f' % 3.1415926 #保留两位小数

'Hello, {0}, 成绩提升了 {1:.1f}%'.format('小明', 17.125) 

r = 2.5 s = 3.14 * r ** 2
print(f'The area of a circle with radius {r} is {s:.2f}')

example 
r = (85-72)/72*100
print('小明的成绩提升了%.1f%%'% r)
print(f'小明的成绩提升了{r:.1f}%')
print('小明的成绩提升了{0:.1f}%'.format(r))

# list
list.append('adam') 插在末尾
list.insert(1, 'adam') 插在位置是index = 1 的地方
list.pop() 删除最后一位
list.pop(1) 删除指定索引的元素
listp[1] = 'adam' 替换

# tuple
a = () 是一个空tuple
定义一位元素的tuple的时候，一定要加逗号避免歧义
tuple里面有list的情况，可以对list里面的数值进行重新赋值，tuple的list也会发生变化

#break结束循环
#continue结束本轮循环，进入下轮循环

# d是一个字典
'Tomas' in d #去判断d中有没有tomas这个key
d.pop('Tomas') #去删除key以及对应的value
dict的key必须是唯一不变的，根据哈希算法。所以list是不能作为key的

# set需要以list作为输入集合，删除重复项//无序和无重复的集合
set([1,2,3])
set.add(4)
set.remove(4)
S1&S2 #交集
S1 | S2 #并集

# def定义函数
#isinstance(x, (int, float)): 判断x是不是后面int或者是float的数据类型
#为了使得我们定义的函数更加完善，那么我们可以添加报错类型
def my_abs(x):
  if not isinstance(x, (int, float)):
    raise TypeError('bad operand type')
  if x >= 0:
    return x
  else:
    return -x
    
#another def    
import math
def quadratic(a, b, c):
    if not isinstance(a, (int, float)):
        raise TypeError('bad operand type')
    if not isinstance(b, (int, float)):
        raise TypeError('bad operand type')
    if not isinstance(c, (int, float)):
        raise TypeError('bad operand type')  
    if a == 0:
        raise TypeError('a should not be assigned as 0')
    if b**2 == 4*a*c:
        return -b/(2*a)
    if b**2 < 4*a*c:
        print('no results')
    if b**2 > 4*a*c:
        x_1 = (-b + math.sqrt(b**2-4*a*c))/(2*a)
        x_2 = (-b - math.sqrt(b**2-4*a*c))/(2*a)
        return x_1, x_2




