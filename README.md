# learning-notes

# Python基础
## 序列：
    可操作索引、切片、相加、相乘和成员资格检查，还可根据内置函数确定序列的长度、找出序列中最大最小的元素。
*索引*:从0开始，-1是索引最后一个元素；可字符串

*切片*:访问特定范围内的元素，可使用两个索引并用冒号隔开；用负数就是从列表最后一个元素开始数。
 
 ，-3代表倒数第三个元素
 ，索引到列表的末尾元素
   ，从列表的首个元素开始索引
 ，复制整个序列
 ，步长为1    ，步长为2
 ，步长为4    
 ，也可从右往左提取元素
*相加*:可使用加法运算来拼接序列，但不同类型的序列不能拼接。
 
（因此如果要对列表中的元素进行加法运算，则需先索引特定元素再进行运算）
*相乘*:将序列与数x相乘时，将重复这个序列x次来创建一个新序列
 
*成员资格*:要检查特定的值是否包含在序列中，可使用运算符in.
 
长度、最大最小值:len()、max()、min()

列表：（list，方括号）
1.	修改列表，给元素赋值
2.	删除元素：del      
 
3.	给切片赋值
一些用于列表的函数用法
append()：用于将一个对象附加到列表末尾
clear()：清空列表的内容
copy()：赋值列表
count()：计算指定的元素在列表中出现了多少次
extend()：能够同时将多个值附加到列表末尾
index()：在列表中查找指定值第一次出现的索引
insert()：用于将一个对象插入列表
     
pop()：从列表中删除一个元素（默认为最后一个元素），并返回这一元素
remove()：用于删除第一个为指定值的元素
reverse()：按相反的顺序排列列表中的元素
sort()：对列表就地排序    
        
sorted()：返回一个有序列表，可用于任何序列
         
高级排序
元组：不可修改的序列（tuple，圆括号）
	
字符串：（str）
	center()：在两边添加字符（默认为空格）让字符串居中
	find()：在字符串中查找子串。如果找到就返回子串的第一个字符的索引，否则返回-1.
	join()：用于合并序列的元素
	lower ()：返回字符串的小写版本
	replace()：指定子串都替换为另一个字符串
	split()：作用与join相反，用于将字符串拆分为序列，如果没有指定符号就默认是空格符号
	strip()：将字符串的开头和末尾的空白（但不包括中间的空白）删除
	translate()：替换字符串的特定部分，只能进行单字符替换

字典：（dict，大括号）   键-值（key+values）
	基本操作：
 
示例：
people = {'Alice': {'phone': '2341','addr': 'Foo drive 23'},
            'Beth': {'phone': '9102','addr': 'Bar street 42'},
            'Cecil': {'phone': '3158','addr': 'Baz avenue 90'}}
labels = {'phone': 'phone number','addr': 'address'}
name = input('Name: ')
request = input('Phone number (p) or address (a)? ')
#使用正确的键
if request == 'p': key = 'phone'
if request == 'a': key = 'addr'
#仅当名字是字典包含的键时才打印信息：
if name in people: print("{}'s {} is {}.".format(name, labels[key], people[name][key]))
Name: Beth
Phone number (p) or address (a)? p
Beth's phone number is 9102.
字典方法：
clear()：删除所有的字典项
copy()：返回一个新字典，其包含的键值对与原来的字典相同（这个方法执行的是浅复制，因为值本身是原件，而非副本）。当替换副本中的值时，原件不受影响。然而，如果修改副本中的值（就地修改而不是替换），原件也将发生变化，因为原件指向的也是被修改的值
 
深复制，可使用模块copy中的函数deepcopy
 
Fromkeys()：创建一个新字典，其中包含指定的键，且每个键对应的值都是None
 
get()：使用它来访问不存在的键时，会返回默认值None，也可指定默认值
items()：返回一个包含所有字典项的列表，其中每个元素都为(key, value)的形式。字典项在列表中的排列顺序不确定
keys()：返回一个字典视图，其中包含指定字典中的键
pop()：用于获取与指定键相关联的值，并将该键-值对从字典中删除。
 
popitem()：类似于list.pop，但list.pop弹出列表中的最后一个元素，而popitem随机地弹出一个字典项，因为字典项的顺序是不确定的，没有“最后一个元素”的概念。
setdefault()：有点像get，因为它也获取与指定键相关联的值，但除此之外，setdefault还在字典不包含指定的键时，在字典中添加指定的键-值对。指定的键不存在时，setdefault返回指定的值并相应地更新字典。如果指定的键存在，就返回其值，并保持字典不变。与get一样，值是可选的；如果没有指定，默认为None。
 
Update()：使用一个字典中的项来更新另一个字典
values()：返回一个由字典中的值组成的字典视图

条件和条件语句：
	if子句、else子句、elif子句
	更复杂的条件：比较运算符、布尔运算符
	while循环
	for循环：遍历特定范围
	跳出循环（break、continue、while True/break）
break示例：假设你要找出小于100的最大平方值（整数与自己相乘的结果），可从100开始向下迭代。找到一个平方值后，无需再迭代，因此直接跳出循环。
 
continue：没有break用得多。它结束当前迭代，并跳到下一次迭代开头。这基本上意味着跳过循环体中余下的语句，但不结束循环。

