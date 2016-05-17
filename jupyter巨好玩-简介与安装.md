# jupyter巨好玩-简介与安装

> ipython notebook改名jupyter了而且更好玩更好用

## jupyter简介

jupyter是啥啊？
这个要从ipython说起，ipython是个交互式的python的解释器，自带颜色，补全还有行号，科学界的很多大牛都用来进行数据分析和图形显示。

ipython还可以运行在浏览器上，就是下面这个样子：

![](http://jupyter.readthedocs.io/en/latest/_images/tryjupyter_file.png)

名字也就高大上一点，叫ipythoon notebook，那个jupyter图标一开始就有的，现在升级改造了，不止于运行python，还有R，spark之类的高大上玩意儿。所以就直接用 jupyter来指代这一对产品了。

官方有个try页面，可以玩一玩。

[https://try.jupyter.org/](https://try.jupyter.org/)

## jupyter安装

官方推荐的安装是这个：
> Download [Anaconda](https://www.continuum.io/downloads). We recommend downloading Anaconda’s latest Python 3 version (currently Python 3.5).

咱们民间可以直接安装
如果已经有python环境：

直接`pip install jupyter`

如果没有：
就先安装个python环境，然后再装

## 运行

`jupyter notebook`

然后就自动打开浏览器中localhost的8888端口，就可以在线写代码啦！不止于python，还有R等...

## 用户界面和主要功能

![](http://nbviewer.jupyter.org/github/ipython-books/minibook-2nd-code/blob/master/chapter1/images/nbui-2.png)

- 写代码
- 写文档（cell类型就分成markdown和code，随便改，所以我这文章都是直接写出来的）
- 科学运算和画图（numpy， scipy，pandas之类的以前都需要一个个安装啊，现在全齐了）

## 示例代码

```python
4+6

```

    10



## 这货是个装饰器


```python
def show_output(func):
    def wrapped(*args, **kwargs):
        output = func(*args, **kwargs)
        print("the result is : ", output)
    return wrapped

```


```python
def is_even(num):
    return num % 2 ==0
```

## 使用装饰器运行函数，并输出结果


```python
f = show_output(is_even)
f(3)

```

    the result is :  False
    

```python

```

## 参考资源

- [http://jupyter.readthedocs.io/en/latest/install.html](http://jupyter.readthedocs.io/en/latest/install.html)
- [https://github.com/lijin-THU/notes-python](https://github.com/lijin-THU/notes-python)  
- [https://github.com/ipython-books/minibook-2nd-code](https://github.com/ipython-books/minibook-2nd-code)
