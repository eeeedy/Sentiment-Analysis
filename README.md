# -
细粒度情感分析
项目名称：细粒度情感分析
项目介绍：本部分采用 AI Challenger 2018 细粒度情感分析比赛数据，该数据为
餐饮领域的用户评论，预先定义 20 个评价对象，并针对每个评价对象进行四分
类，数据样例如下图所示。
其中，-2 表示未提及，-1 表示负面情感，0 表示中性情感，1 表示正面情感。
在该数据上完成分类任务，评价指标采用各评价对象宏平均 F1 值的平均值。

（1）基础任务：
分别采用 LSTM、BERT 进行分类，参考 F1 值分别为 60%，70%。
（2）进阶任务：
采用文档级层次化注意力网络 HAN 进行分类，参考 F1 值为 64%。
模型论文为《Hierarchical Attention Networks for Document Classification》。
（3）高阶任务：
上述任务实现过程中，可针对每个评价对象训练一个模型，但这在实际使用
中代价较大。尝试在 BERT 的基础上改进，只训练一个模型，能够同时进行所有
评价对象的分类。
