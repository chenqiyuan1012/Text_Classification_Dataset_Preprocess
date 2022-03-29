# Text_Classification_Dataset_Preprocess
常见的文本分类数据集，以及相关的处理代码，可以将所有数据集处理为相同格式，便于模型输入

# 数据集地址

[数据集地址](https://drive.google.com/drive/folders/0Bz8a_Dbh9Qhbfll6bVpmNUtUcFdjYmF2SEpmZUZUcVNiMUw1TWN6RDV3a0JHT3kxLVhVR2M?resourcekey=0-TLwzfR2O-D2aPitmn5o9VQ)

使用Google Drive存储，需要科学上网

其中包括：ag_news, amazon_review, dbpedia, sogou_news, yelp_review, yahoo_answers

[IMDB数据集](http://ai.stanford.edu/~amaas/data/sentiment/)

下载后将Train等文件夹直接放在IMDB文件夹下即可

## 格式
最终的数据集有三种类型，训练集，无监督训练集和测试集，均为CSV文件

其中训练集和测试集的格式为

label,sentence，可以使用pandas中的read_csv来读取

无监督训练集的格式为

sentence

# 处理方法
## IMDB
IMDB数据集中原有25000条有监督数据，25000条训练数据和50000条无监督数据，对于测试数据保持不变。对于有监督数据，从中随机采样20/500/2500条样本，各个标签数量平均分布。将其余的有监督样本去除标签后和无监督样本混合，采样70000条，得到无监督数据。

## yahoo_answers

将问题和回答合并
