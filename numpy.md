1. #### numpy 产生随机书的方法

a. randint: 原型：numpy.random.randint\(low, high=None, size=None, dtype='l'\)，产生随机整数；

b. random\_integers: 原型： numpy.random.random\_integers\(low, high=None, size=None\)，在闭区间上产生随机整数；

c. random\_sample: 原型： numpy.random.random\_sample\(size=None\)，在\[0.0,1.0\)上随机采样；

d. random: 原型： numpy.random.random\(size=None\)，和random\_sample一样，是random\_sample的别名；

e. rand: 原型： numpy.random.rand\(d0, d1, ..., dn\)，产生d0 - d1 - ... - dn形状的在\[0,1\)上均匀分布的float型数。

f. randn: 原型：numpy.random.randn（d0,d1,...,dn\),产生d0 - d1 - ... - dn形状的标准正态分布的float型数。

g.uniform\(low,high,size\)  从一个均匀分布\[low,high\)中随机采样，注意定义域是左闭右开，即包含low，不包含high.the minimum 



1. #### numpy int 和float类型的最大值和最小值

```
for dtype in [np.int8,np.int32,np.int64]:
    print('the minimum value of {}:'.format(dtype),np.iinfo(dtype).min)
    print('the maximum value of {}:'.format(dtype),np.iinfo(dtype).max)
for dtype in [np.float32,np.float64]:
    print('the minimum value of {}:'.format(dtype),np.finfo(dtype).min)
    print('the maximum value of {}:'.format(dtype),np.finfo(dtype).max)class 'numpy.int8'

the minimum value of <class 'numpy.int8'>: -128
the maximum value of <class 'numpy.int8'>: 127
the minimum value of <class 'numpy.int32'>: -2147483648
the maximum value of <class 'numpy.int32'>: 2147483647
the minimum value of <class 'numpy.int64'>: -9223372036854775808
the maximum value of <class 'numpy.int64'>: 9223372036854775807
the minimum value of <class 'numpy.float32'>: -3.40282e+38
the maximum value of <class 'numpy.float32'>: 3.40282e+38
the minimum value of <class 'numpy.float64'>: -1.79769313486e+308
the maximum value of <class 'numpy.float64'>: 1.79769313486e+308
```

#### 



