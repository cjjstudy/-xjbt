# 2019-04-02
kNN
交叉验证：
1、一般是数据分为训练集和测试集。
在测试集上可能会出现过拟合的情况。 此时，测试集上的信息反馈足以颠覆训练好的模型。所以再分出一个验证集，模型训练完成以后在验证集上对模型进行评估。 当验证集上的评估实验比较成功时，在测试集上进行最后的评估。
然而，通过将原始数据分为3个数据集合，我们就大大减少了可用于模型学习的样本数量， 并且得到的结果依赖于集合对（训练，验证）的随机选择。

2、这个问题可以通过 交叉验证（CV 缩写） 来解决。 交叉验证仍需要测试集做最后的模型评估，但不再需要验证集。
   最基本的方法被称之为，k-折交叉验证 ：
   将 k-1 份训练集子集作为 training data （训练集）训练模型，
将剩余的 1 份训练集子集作为验证集用于模型验证（也就是利用该数据集计算模型的性能指标，例如准确率
# 2019-04-03
决策树
extend是把列表所有元素与之前合并，而append是把列表当做一个整体与之前合并




函数说明:创建绘制面板
   fig.clf()

#2019-04-04
朴素贝叶斯
1、定义loadDataSet() 输入数据
   包含postingList数据集（每一行一个文档，[ [],[] ])
      classVec类别标签（1包含侮辱性文字，0全部正常 [] )
   并返回
2、定义createVocabList(dataSet) 得到不重复数据
   def createVocabList(dataSet):
       vocabSet = set([])
       for document in dataSet:
           vocabSet = vocabSet|set(document)
       return list(vocabSet)
   注意：dataSet用上面返回数据值
   返回形式vocabSet，即不重复的数据
3、定义setOfWords2Vec(vocabList,inputSet)
















