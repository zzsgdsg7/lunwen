# lunwen
垃圾学生的论文代码（我是真的菜）

2021.12.22：
{
  基于改进的k-shell方法识别复杂网络中有影响力的重要节点（主要是基于K-shell和信息熵EI）
  介绍了IKS算法：
   1：根据K壳法分解网络，得到KS值
   
   2：计算信息熵
   
   3：排序，每个K层的节点按照节点信息熵的大小进行排序
}

2021.12.23
{
  1：查找到了iks的代码
  
  2：将jazz网络图用gephi进行了可视化
  
}

2021.12.24
{

  1:今天准备实现k-shell算法，将它应用于经典网络集，挖掘出关键节点
  
}

2021.12.27
{

  1.周一完全没有任何的想法，看一下经典centrality代码，然后将他们运用于Karet数据集上试一试，上周五将K-shell算法运用上去之后，感觉剥离出来的层数有误，只有ks=1和ks=2的两层，不知道怎么回事，代码上还要再看一看！
  
  2.论文思考：能否将ksgc算法与网络结构识别法相结合？ksgc算法是将K-shell算法和GC算法相结合，提出了一个修正系数，然后在修正系数的作用下计算，最后排序出来节点重要性。网络结构识别，首先也是将网络进行k-shell分解，然后计算出每个节点在ks分解中的迭代次数NIM，在这一步给出了网络中节点的全局重要性以及它们如何被网络中的其他节点所包围。在计算NIM之后，结合节点的度值，KS值和NIM计算节点的归一化全局重要性NGI，最后考虑领域计算出节点的相对局部——全局重要性(RLGI)，最后对节点进行归一化排名。
  
  3.<font color = red >能否将NGI这一步中的KS值换为KSGC值？</font>
  
  4.每一个站点的时间序列分析！感觉这一点有很多东西可以挖掘
  
}

2021.12.28

{

  1.每一个站点的时间序列图太密集，注意到原始数据上，分辨率是以每小时来记录的，想把数据的分辨率转换成每日均值，这样的话，观察每日的数据量。
  
  2.今天居然找到了KSGC的代码，csdn大佬yyds！！！我肯定是第一个看到这串代码的人

}

2022.01.04

{
  1.元旦三天都在胡吃海喝，今天开始新年工作的第一天。
  
  2.重新看KSGC论文中的评价指标，在经典数据集中跑一下代码，查看算法的精确度。其中评价指标有：DC,BC,CC和EC，来探究与KSGC的关系，验证KSGC方法的正确性，感觉自己的论文不需要这一步。测试算法的性能，与一些最先进的基于K-shell方法进行对比，如混合度分解(MDD)、分层K壳法(HKS)、改进的K壳混合(KSHI)、K壳迭代因子(KS-IF)和基于潜在边权重的K壳指数(WKS)，基于重力模型的方法(GC和WGC)进行比较。
  
}

2022.01.06

{
  1.首先建立四川省空气质量网络。
  
  2.对于风速数据，将同一城市监测站点的风速进行相同化处理，将各污染物进行季节化分析。

}
