## Some highlights of the paper

When trained on large-scale datasets, deep ConvNets do not require the knowledge of words, in addition to the conclusion from previous research that ConvNets do not require the knowledge about the syntactic or semantic structure of a language. 

Dataset size forms a dichotomy between traditional and ConvNets models: the larger datasets tend to perform better.  

ConvNets may work well for user-generated data.  

---

#### Text Classification:

a.  文本分类的概念

文本分类就是将一句或者一段文本内容分到指定的类别。文本分类是自然语言处理的基础任务，应用于自然语言处理的各个领域，如信息检索，信息过滤，垃圾邮件分类。

b.  两种基于词向量和卷积神经网络的文本分类模型

基于词向量和分类模型就是将一句话中的每个词表示成词向量，然后这句话将可以表示成一个矩阵，然后使用卷积神经网络分类模型即可对文本进行分类。

c.  CNN的相关概念

本文使用的是一维卷积，对于一维卷积，需要了解卷积核的尺寸，卷积核个数，步长以及padding这些概念。

The History of Text Classification:

~ 1950 - 1980: Apply experts' rules to do classification 

~ 1980 - 1990: Expert's system: use knowledge engineering to build expert system

~ 1990 - 21st century: machine learning: feature engineer and some models such as SVM, KNN, decision tree, ...

- feature engineering: 
  - frequency of each words
  - TF-IDF
  - N-gram info
- feature selection and feature reduction:
  - information gain (信息增益), Mutual information (互信息),
  - PCA, SVD

~ 2013 - present: deep learning: word vector + NN