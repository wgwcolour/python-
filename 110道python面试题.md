1、一行代码实现1-100之和

```python
sum(i for i in range(100))
```

2、如何在一个函数内部修改全局变量

```python
v = 1
def fun():
    global v
    v = 2
fun()
v #v = 2
```

3、列出5个python常用标准库

```python
datetime; os; sys; re; json;
```

4、字典如何删除键？如何合并两个字典？

```python
dic = {'a':1,'b':2}
dic1 = {'c':3,'d':4}
# 删除
dic.pop('a') # 返回被删除的值
del dic['a'] # 无返回值
# 合并字典
dic.update(dic1) #还有其他方法
```

5、谈下python的GIL

``` 暂无```

6、python实现列表去重的方法

```python
li = []
list(set(li))
```

7、```fun(*args,**kwargs)```中*args,**kwargs是什么意思？

```python
*args是不定数量的位置参数。

**kwargs是不定数量的关键字参数。
```

8、python2和python3中的range(100)有什么区别？

```python
python2的range方法生成一个列表，xrange是生成器写法，占用很小的内存。
python3统一为range生成器写法。
```

9、一句话解释什么样的语言能用装饰器？

```动态语言？题目什么意思没明白```

10、python内建数据类型有哪些？

```python
不可变：元组、集合、字符串、数字
可变：列表、字典
```

11、简述面向对象中```_new_```和```_init_```的区别

```python
在class中使用这两种方法：在这个类实例化以后，执行初始化init方法能够赋予类属性。使用new方法，是在实例化之前，执行new方法返回一个类。
```

12、简述with方法打开处理文件帮我们做了什么？

```python
with方法能够在打开文件代码块执行完毕后，close文件。在异常是同样如此。
```

13、列表[1,2,3,4,5]请使用map()函数输出[1,4,9,16,25]，并使用列表推导式提取出大于10的数。

```python
li = [1,2,3,4,5]
[i for i in map(lambda x:x**2,li)] #[1,4,9,16,25]
[i for i in map(lambda x:x**2,li) if i > 10] # [16,25]
```

