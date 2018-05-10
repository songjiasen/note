### 简介
数据结构是用来存储一组相关数据的。
Python中有四种内建的数据结构--列表（list）、元组（tuple）、字典（dict）和集合（set）。

### list
列表（list）是处理一组有序项目的数据结构。在Python中每个项目中间用逗号分隔。列表中的项目应该包括在方括号中。在列表中可以任意添加、删除或是搜索列表中的元素。

例：

		>>> test = ['a','b','c']

变量`test`就是一个list，可以用`len()`函数获得它的长度

用索引来访问list中每一个位置的元素

		>>> test[0]
		'a'
		>>> test[1]
		'b'
		>>> test[-1] #取最后一个元素可以用-1做索引
		'c'
		>>> test[-2] #倒数第二个
		‘b’
		
list是一个可变的有序表，所以可以追加元素到list的末尾
		
		>>> test.append('d')

加到指定位置
		
		>>> test.insert(1,'e')
		
可以用pop()方法删除list末尾的元素,加参数可以删除指定元素

		>>> test.pop()
		>>> test.pop(1)

### tuple
元组（tuple）。tuple和list非常类似，但是tuple一旦初始化就不能修改。

例：

		>>> test = （'a','b','c'）
		
现在，test这个tuple不能变了，它也没有append()，insert()这样的方法。其他获取元素的方法和list是一样的，你可以正常地使用test[0]，test[-1]，但不能赋值成另外的元素。



