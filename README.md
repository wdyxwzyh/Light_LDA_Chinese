# Light_LDA_Chinese
中文分布式LDA主题模型

  ** 开发阶段 先占坑 
  ** 在进行gensim段落主题聚类时遇到千万级数据导致cpu拉满、内存爆掉的问题 发现巨硬有分布式的lightlda项目
  ** 尝试在此项目基础上开发中文分布式gensim lda

  ** 主要问题:
    1、lda模型复杂度取决于topic k及dict v的大小 还要考虑内存中的复制等 需要空间一般是3kv
      可通过filter_extremes降低字典大小、 降低topic数量 、降低数据量来应急 但是都治标不治本
    2、巨硬已经实现的的模式为1000个topic 
