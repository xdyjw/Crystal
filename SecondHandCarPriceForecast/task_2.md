## 数据探索性分析
---
### 数据初步分析（采用pandas函数）

- 载入数据
```python
    data = pd.read_csv(file, sep='')
```

- 查看原始数据
```python
    data.head()
```

- 查看数据的列名
```python
    data.colums()
```

- 查看数据字段的完整数量和类型
```
    data.info()
    # 资料 https://vimsky.com/examples/usage/python-pandas-dataframe-info.html
```

- 查看初步统计量
```python
    data.describe()
```
    - 一般统计量包括
        - 均值
        - 方差
        - 最大值
        - 最小值

- 缺失值分析
```python
    # 缺失数量统计
    data.isnull().sum()
```
    - 缺失处理方法
        - 如果很少就填充
        - 如果很多可以考虑删除这个字段
    - 填充方法
        - 利用树模型进行填充
        - 均值预估

- 异常值分析
```python
    # 分析类别特征值的数量
    data['field'].value_counts()
```
    - 判断方法
        - 对于类别特征，如果严重倾斜，可以删掉
        - 对于连续特征，可以进行分桶分析
        
- 预测值分析
```python
    # 拟合分布
    import scipy.stats as st

    plt.figure(1); plt.title('Johnson SU')
    sns.distplot(y, kde=False, fit=st.johnsonsu) # 约翰逊分布

    plt.figure(2); plt.title('Normal')
    sns.distplot(y, kde=False, fit=st.norm) # 正态分布

    plt.figure(3); plt.title('Log Normal') # 对数正态分布
    sns.distplot(y, kde=False, fit=st.lognorm)

    # 偏度峰度分析 https://www.cnblogs.com/wyy1480/p/10474046.html
    sns.distplot(y);
    print("Skewness: %f" % y.skew())
    print("Kurtosis: %f" % y.kurt())

    # 分桶分析
    plt.hist(y, orientation = 'vertical', histtype = 'bar', color ='red')
    plt.show()
```
    - 分析方法
        - 拟合
        - 偏度峰度分析
        - 分桶分析

    
