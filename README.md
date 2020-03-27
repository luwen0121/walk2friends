
## 示例用法
--input example_graphs/karate.adjlist --output karate.embeddings
**--input**:  *input_filename*
``--format mat``用于包含邻接矩阵的mat.mat文件，必须指定邻接矩阵的变量名`--matfile变量名`
skipgram格式的输出表示-第一行是header，所有其他行是node id和*d*维度表示：
示例：
        34 64
        1 0.016579 -0.033659 0.342167 -0.046998 ...
        2 -0.007003 0.265891 -0.351422 0.043923 ...
        ...
命令行示例：
 walk2friends --format mat --input example_graphs/blogcatalog.mat
    --max-memory-data-size 0 --number-walks 80 --representation-size 128 --walk-length 40 --window-size 10
    --workers 1 --output example_graphs/blogcatalog.embeddings
    
最大内存数据大小0--数字行走80--嵌入大小128--行走长度40--窗口大小10
--workers 1——输出示例图/blogcatalog.embeddings
workers调大可以更快的训练（多核机器，单核就是1）

所需相关库：
wheel>=0.23.0
Cython>=0.20.2
argparse>=1.2.1
futures>=2.1.6
six>=1.7.3
gensim>=1.0.0
scipy>=0.15.0
psutil>=2.1.1
networkx>=2.0

