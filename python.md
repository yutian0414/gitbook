1. ##### 可以对字节串做类似与字符串对操作（查找，开头，slice等）如果匹配字节串，正则表达式对匹配模式使用b开头，如`b'[; ,]]`
2. ##### `round(value,ndigits)`将小数取整，并保留ndigits位小数
3. ##### decimal 模块，可以提供更高精度对数学运算。
4. ##### format\(x, '0.2f'\)  x=123.45  format 用于格式化输出数字 str.format\('  '\) 用于字符串对格式化， 格式为'\[&lt;&gt;^\]？width\[,\]?\(.digits\)?' \[\] 中对值为可选值，width，和digits 为整数
5. ##### 使用`bin(), oct(), hex()` 可以转化为相应的进制
6. ##### 正负无穷大对表示方法   `float('inf')   float('-inf')    math.isinf(a)`来判断是否是无穷大  float\('nan'\)  math.isnan\(c\)
7. ##### fractions 用于处理涉及到分数对数学计算
8. ##### random.choice\(\[1,2,3,\]\)  选择一个       random.sample\(\[1,2,3,4,5\], 3\) 取样     random.shuffle\(value\_list\)  洗牌
9. ##### random.randint\(0,10\) 0到10之间对随机整数     random.random\(0,1\)  0到1之间对随机float数
10. ##### random.seed\(\)  用来初始化种子
11. ##### calender  模块 处理与日历相关对内容
12. ##### datetime.strptime\(text,'%Y-%m-%d'\)
13. ##### pytz 模块处理有关时区的问题
14. ##### 通常处理本地时间的方法是将所有对日期都转化微UTC时间，然后将所有对内部存储和处理都使用UTC时间
15. ##### reversed\(\) 可以实现反向迭代， for x in reversed\(a\)              要求待处理对象拥有可确定的大小，或者实现了\_\_reversed\(\)\_\_特殊方法时才有效            可以先转化为列表，然后使用reversed\(value\_list\)来实现

> ```py
>                                        class countdown:
>                                            def __init__(self,start):
>                                                self.start=start
>                                            def __iter__(self):
>                                                while n>0:
>                                                n=self.start
>                                                yield n
>                                                n-=1
>                                            def __reversed__(self):
>                                                n=1
>                                                while n<=self.start:
>                                                yiled n
>                                                n+=1
> ```

1. ##### itertools.islice\(\)  可以用来对迭代器和生成器进行切片操作，itertools.dropwhile\(a\)  可对对于返回为True的项目忽略掉，即迭代时跳过前面的某些项目，直到有不满足项目的出现，后面的返回True的项目也不忽略
2. ##### itertools.permutations\(vale_list or value \_set\)  用来讲其中的元素的所有排列情况返回。 itertools.permutations\( value\_list, num\)  用于产生序列中num个元素的组合情况，其中一个元素在一次组合中只能选一次，itertools.combinations\_with\_replacement\(value\_list,num\) 可以允许在一次组合时，一个元素可以选择多次_
3. ##### enumerate\(value\_lis, num\)  迭代时可以返回列表的序号, num 表示排序从num开始计数
4. ##### zip\(a, b, c...\) 产生一个\[（a\[i\], b\[i\], c\[i\]...\).......\] 的元组列表迭代器      itertools.ip\_longest\(a, b, fillvalue\)可以不要求a和b的长度一致，长度不足的使用fillvalue填充
5. ##### for x in  itertools.chain\(a,b,c\)  可实现对a，b，c集合的所有元素进行迭代，效率比  for x in a+b+c 要高，因为不会产生一个新的变量。
6. ##### yield from iterable 本质上等于  for item in iterable :yield item  的缩写。
7. ##### heapq.merge\(a, b\)  可以对有序序列，进行有序和并，并且可以进行有序的迭代。要求a和b都是预先拍好序的，它会取a\[0\]同b\[0\]进行比较，然后先返回小的，在返回大的，然后查看a\[1\]和b\[1\]
8. ##### iter\(\) 函数，可以选择性接受yield无参数的可调用对象以及一个哨兵（结束）值作为输入，iter\(\)会创建一个迭代器，然后重复调用用户提供的可调用对象，知道返回哨兵值为止
9. ```py
   CHUNKSIZE=8129
   def reader(s)
       while True:
           data=s.recv(CHUNKSIZE)
           if data == b'':
               break
           process_data(data)
   #可以使用iter()改写为如下的形式
   def reader(s):
       for chunk in iter(lambda:s.recv(CHUNKSIZE), b''):
           process_data(data)
   ```

9. open打开文件模式  rt 读，wt写，at追加  with open\('sample.txt', 'rt', encoding='utf-8', errors='ignore'\)  ignore 还可以为replace

```py
with open('somefile.txt', 'rt') as f:
    print('hello world', file=f)
    
```

print 中增加一个file，可以讲打印内容重定向到文件中



