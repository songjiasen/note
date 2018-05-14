### dict
dict使用键-值（key-value）存储，具有极快的查找速度。
例：

	>>> d = {'Michael': 95, 'Bob': 75, 'Tracy': 85}
	>>> d['Michael']
	95
	
#### 与list的区别：

* dict的第一个特点是查找速度快，无论dict有10个元素还是10万个元素，查找速度都一样。而list的查找速度随着元素增加而逐渐下降。不过dict的查找速度快不是没有代价的，dict的缺点是占用内存大，还会浪费很多内容，list正好相反，占用内存小，但是查找速度慢。

* 由于dict是按 key 查找，所以，在一个dict中，key不能重复。

* dict的第二个特点就是存储的key-value序对是没有顺序的！

写给php程序员：
	
	$test1 = array('a','b');
	$test2 = array(
			'index1' => 'a',
			'index2' => 'b'
		);
		
形式上来讲$test1为python中的list类型，$test2为python中的dict类型

往dict添加数据

	>>> d['Jack'] = 90
	>>> d['Jack']
	90
	>>> d['Jack'] = 88
	>>> d['Jack']    #会覆盖
	88
	
通过dict提供的get()方法取数据，如果key不存在，可以返回None，或者自己指定的value：
	
	>>> d.get('Thomas')
	>>> d.get('Thomas', -1)
	-1
	
要删除一个key，用pop(key)方法，对应的value也会从dict中删除：
	
	>>> d.pop('Bob')
	75
	>>> d
	{'Michael': 95, 'Tracy': 85}
	
* 请务必注意，dict内部存放的顺序和key放入的顺序是没有关系的；dict的key必须为不可变的类型

### set

set和dict类似，也是一组key的集合，但不存储value。由于key不能重复，所以，在set中，没有重复的key。

要创建一个set，需要提供一个list作为输入集合.

重复元素在set中自动被过滤：

	>>> s = set([1, 1, 2, 2, 3, 3])
	>>> s
	{1, 2, 3}

通过add(key)方法可以添加元素到set中，可以重复添加，但不会有效果：

	>>> s.add(4)
	>>> s
	{1, 2, 3, 4}
	>>> s.add(4)
	>>> s
	{1, 2, 3, 4}
	
通过remove(key)方法可以删除元素：

	>>> s.remove(4)
	>>> s
	{1, 2, 3}

通过pop()方法来获取并删除元素

	>>> s
	{1, 2, 3}
	>>> s.pop()
	1
	>>> s
	{2, 3}

set可以看成数学意义上的无序和无重复元素的集合

