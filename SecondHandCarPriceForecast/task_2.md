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
