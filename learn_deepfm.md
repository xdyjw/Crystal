## 总结
- 提升ctr模型表现方法：特征组合
- 特征组合的方法
  - FM
  - FFM
  - FNN
  - PNN
  - DNN
- 低阶特征组合
  - FM FFM
- 高阶特征组合
  - DNN
- FM和DNN的结合方式
  - 串行：缺点是低阶组合特征学习到的比较少，DNN的全连接结构导致低阶特征并不能在DNN的输出端较好的表现
  - 并行
- 网络结构
  - FM Layer是由一阶特征和二阶特征Concatenate到一起
  - Dense Embeddings就是为了解决DNN中的参数爆炸问题
  - 



