部分方法的开源代码地址以及实验部分设置

开源代码：
- EHCF：https://github.com/chenchongthu/EHCF
- GHCF：https://github.com/chenchongthu/GHCF
- MB-GMN：https://github.com/akaxlh/MBRec
- CML：https://github.com/weiwei1206/CML.git
- BCIPM：https://github.com/MingshiYan/BIPN
- COPF： https://github.com/1918190/COPF
- HEM-GNN：https://github.com/SamuelZack/MultiRec
- S-MBRec：https://github.com/GuShuyun/MBRec
- CRGCN：https://github.com/MingshiYan/CRGCN
- MB-CGCN：https://github.com/SS-00-SS/MBCGCN
- MMCLR：https://github.com/wyqing20/MMCLR
- Disen-CGCN：https://github.com/JianhuaDongCS/Disen-CGCN
- DA-GCN：https://github.com/xizhu1022/DA-GCN
- MBSSL：https://github.com/Scofield666/MBSSL.git
- DeMBR：https://github.com/DeMBR2024/DeMBR.git
- POGCN：https://anonymous.4open.science/r/POGCN-E8FD
- HEML：https://github.com/Breeze-del/HEMLCODE

实验设置：

  为直观体现基于GNN的多行为推荐方法的发展和性能，本文选择部分代表性的模型，在两个真实数据集上进行验证。贝贝（https://www.beibei.com），来自中国最大的婴幼儿用品电商平台，用户以母婴群体为主，商品种类较为集中。淘宝（https://tianchi.aliyun.com/dataset/dataDetail?dataId=649），来自中国最大的电商平台——阿里巴巴，其用户群体复杂，商品种类相对广泛。两个数据集均包含浏览、加购物车和购买行为数据。本文将“购买”视为目标行为，“浏览”和“加购物车”视为辅助行为。
  
  本文保留每个数据集最早的交互，并且合并重复的交互记录，然后过滤掉购买记录少于5次的用户和项目，最后根据行为类别和时间顺序将剩余的数据集划分为训练集、验证集和测试集。其中，用户的最后一条购买记录被作为测试数据，倒数第二条被作为验证数据，其余作为训练数据。
  
  本文的实验运行环境基于Ubuntu操作系统，深度学习加速器为NVIDIA GeForce RTX 4090显卡。实验环境通过Anaconda管理，采用PyTorch 1.12.1框架实现模型训练，并分别使用Xavier方法和Adam优化器对模型参数进行初始化和优化。按照各方法的原始设置，本文将CML方法的嵌入维度设置为32维，其余方法的维度设置为64维。另外，将BCIPM的数据集批次大小（Batch Size）设置为1024，将EHCF、MBSSL和CML设置为512，其余方法均设置为256。关于模型学习率，本文统一设置为1e-3。为保证性能对比的严谨性和公平性，各模型的其他超参数均严格按照原文公布的数据进行配置。

