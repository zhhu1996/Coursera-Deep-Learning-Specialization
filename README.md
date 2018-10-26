# Deep Learning Specialization
## Andrew Ng, 吴恩达
## 传送门: https://www.coursera.org/specializations/deep-learning
1. Neural Networks and Deep Learning  
- 深度学习介绍:   
    - CNN, RNN   
    - structured data, unstructured data;   
    - Idea, Code, Experiment  
- 深度学习基础  
    - 流程     
        - 前向传播计算代价函数  
        - 反向传播计算偏导数  
        - 优化  
    - Python广播机制  
- 浅层神经网络(1个隐藏层)      
    - 线性函数  
    - 激活函数    
    - 权重系数随机初始化(应尽量小)    
- 深度神经网络(多个隐藏层)  
    - 系数矩阵的维度  
    - 超参数:  
        - learning_rate  
        - #iteration  
        - #hidden layer L  
        - #hidden units  
        - choice of activation function  
          
2. Improving Deep Neural Networks: Hyperparameter tuning, Regularization and Optimization  
- 深度学习实践   
    - 训练集/开发集/测试集  
        - 中量数据: 70/30 or 60/20/20  
        - 大量数据: 98/1/1  
    - 偏差和方差
        - 高偏差: 更大的神经网络，训练更长的时间
        - 高方差: 更多的数据，正则化
    - 正则化  
        - L2正则化  
        - dropout
        - 数据增补  
        - 早停止  
    - 建议
        - 输入归一化  
        - 挑选合适的权重进行初始化(He)  
        - 梯度检测  
- 优化算法  
    - 小批量梯度下降  
        - 1 < size < m  
        - mini-batch size = 64, 128, 256, 512  
    - 指数加权滑动平均  
        - 1/(1-beta)时间内的平均值
        - 偏差修正  
    - Momentum  
        - 对dw, db进行滑动加权平均
        - beta=0.9效果较好  
        - 一般不进行偏差修正  
    - RMSprop  
        - 对dw^2, db^2进行滑动加权平均  
        - epsilon=10^-8效果较好
        - 一般不进行偏差修正  
    - Adam  
        - 结合了Momentum + RMSprop
        - 偏差修正 
        - 效果非常好  
    - 学习率衰减  
        - 在优化过程中不断改变学习率  
        - 较晚考虑  
- 超参数搜索, 批量归一化和编程框架  
    - 超参数搜索  
        - 随机搜索  
        - 线性平均随机搜索  
        - 指数平均随机搜索  
    - 批量归一化  
        - 训练集: 代入公式   
        - 测试集: 对训练集的参数进行滑动加权平均  
    - 多类别分类  
        - softmax  
        - 交叉熵  
    - 深度学习框架  
        - Tensorflow

3. Structuring Machine Learning Projects  
- 机器学习策略1  
    - 正交化超参数  
    - 设置单一的量化评估指标  
        - (准确率，召回率) -> F1-score
        - 优化指标(1个)和满足指标(N-1个)
    - 开发集/测试集
        - 必须来自同一分布
        - 必须随机选取
    - 修改评估指标
    - bias/varience权衡
        - bayes error
        - avoidable bias
        - varience  
    
4. Convolutional Neural Networks
5. Sequence Models
