###简介
开发过程中通常使用函数来实现代码的可重复调用，但是如果代码越写越多，一个文件中函数数量过多就会造成代码可读性降低并且不容易维护。

这时候就会有计划的将一些功能类似或者属于一块内容的函数来进行分组，分别放到不同的文件中来进行保存，这样每个文件保持相对较少的代码量，提高可读性和可维护性，需要的时候引入这些文件来调用里面的函数。

其中每一个文件便是一个模块。

### 模块的`__name__`

每个模块都有一个名称，在模块中可以通过语句来找出模块的名称。当一个模块被第一次输入的时候，这个模块的 主块将被运行。假如我们只想在程序本身被使用的时候运行主块，而在它被别的模块 输入的时候不运行主块，我们该怎么做呢?这可以通过模块的 `__name__` 属性完成。

例子:

	#!/usr/bin/python	# Filename: using_name.py	if __name__ == '__main__':	print('This program is being run by itself')	else:	print('I am being imported from another module')

输出:

	$ python using_name.py	This program is being run by itself	$ python	>>> import using_name	I am being imported from another module	>>>

> 每个 Python 模块都有它的 `__name__`，如果它是`__main__`，这说明这个模块被用户单独运行，我们可以进行相应的恰当操作。

### 第三方模块

Python通过包管理工具pip来安装第三方包，Mac环境自带python2对应的命令为pip，如果自己安装了python3则对应的pip命令为pip3

pip安装包的语句为 `pip install package`

一般来说，第三方库都会在Python官方的pypi.python.org网站注册，要安装一个第三方库，必须先知道该库的名称，可以在官网或者pypi上搜索
