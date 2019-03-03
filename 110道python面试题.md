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

14、python中生成随机整数、随机小数、0—1之间小数方法 

```python
import random
random.randint(0,100)# 0-100随机整数
random.uniform(0,100) # 0-100随机小数 
random.random() # 0-1之间随机小数
```

15、避免转义给字符串加哪个字母表示原始字符串？ 

```python
r'str'
```

16、```<div class="nam">中国</div>```，用正则匹配出标签里面的内容（“中国”），其中class的类名是不确定的 

```python
import re
html = '<div class="nam">中国</div>'
rule = re.compile('>(.*?)<')
nam = re.findall(rule,html)[0]
```

17、python中断言方法举例 

```python
a = 2
assert a == 3 # 将报错：AssertionError
```

18、数据表student有id,name,score,city字段，其中name中的名字可有重复，需要消除重复行,请写sql语句 

```sql
select distinct name from student --查询出name并排重。。
```

19、10个Linux常用命令 

```python
暂无
```

20、python2和python3区别？列举5个 

```puyhon
print、range(xrange)、class(object)、？
```

21、列出python中可变数据类型和不可变数据类型，并简述原理 

```python
不可变：元组、集合、字符串、数字
可变：列表、字典
原理：？
```

22、s = “ajldjlajfdljfddd”，去重并从小到大排序输出”adfjl” 

```python
print(''.join(sorted(set(s))))
```

23、用lambda函数实现两个数相乘 

```python
lambda x,y:x*y
```

25、利用collections库的Counter方法统计字符串每个单词出现的次数”kjalfj;ldsjafl;hdsllfdhg;lahfbl;hl;ahlf;h” 

```python
不会？
```

26、字符串a = “not 404 found 张三 99 深圳”，每个词中间是空格，用正则过滤掉英文和数字，最终输出”张三  深圳” 

```python
import re
rule = re.compile("[a-z]+\s[0-9]+\s[a-z]+\s|99")
re.sub(rule,'',a)
```

27、filter方法求出列表所有奇数并构造新列表，a =  [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 

```python
def j(n):
    if n%2 == 1:
        return n
[i for i in filter(j,a)]
```

28、列表推导式求列表所有奇数并构造新列表，a =  [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 

```python
[i for i in a if i%2==1]
```

29、正则re.complie作用 

```python
构建一个过滤规则
```

30、a=（1，）b=(1)，c=(“1”) 分别是什么类型的数据？ 

```python
tuple，int，string
```

31、两个列表[1,5,7,9]和[2,2,6,8]合并为[1,2,2,3,6,7,8,9] 

```python
题目错了吧？
sorted([1,5,7,9]+[2,2,6,8])
```

32、用python删除文件和用linux命令删除文件方法 

```python
不会？
```

33、log日志中，我们需要用时间戳记录error,warning等的发生时间，请用datetime模块打印当前时间戳 “2018-04-01 11:38:54” 

```python
import datetime
datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")
```

34、数据库优化查询方法 

```python
优化sql语句，建索引，不使用select *……
```

35、请列出你会的任意一种统计图（条形图、折线图等）绘制的开源库，第三方也行 

```python
pyecharts
```

36、写一段自定义异常代码 

```python
a = 1
if a == 1:
    raise TypeError("类型错误")
```

37、正则表达式匹配中，（.*）和（.*?）匹配区别？ 

```python
贪婪匹配和非贪婪匹配。贪婪匹配会尽可能多的匹配结果，非贪婪匹配相反。好像有点问题。(.)是一个任意字符，(.?)是什么呢
```

38、简述Django的orm 

```python
不会呀？
```

39、[[1,2],[3,4],[5,6]]一行代码展开该列表，得出[1,2,3,4,5,6] 

```python
[i for s in [[1,2],[3,4],[5,6]] for i in s]
```

40、x=”abc”,y=”def”,z=[“d”,”e”,”f”],分别求出x.join(y)和x.join(z)返回的结果 

```python
dabceabcf
dabceabcf
```

