# Spark 学习



## Spark 核心概念简介



每个Spark 应用都由一个驱动器程序( **driver program** ) 来发起集群上的各种并行操作，驱动器程序包含应用的 main 函数，并且定义了集群上的分布式数据集，还对这 些分布式数据集应用了相关操作。 

驱动器程序通过一个 **SparkContext** 对象来访问 Spark。这个对象代表对计算集群的一个连接，一旦有了 **SparkContext**，你就可以用它来创建 **RDD**。 

驱动器程序一般要管理多个执行器(**executor**)节点。比如，如果我们在 集群上运行 count() 操作，那么不同的节点会统计文件的不同部分的行数。 

