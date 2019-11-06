##  Background Knowledge 

- [CNN](https://www.zhihu.com/question/52668301/answer/131573702) 
- One-hot encoding

## Some highlights of the paper

When trained on large-scale datasets, deep ConvNets **do not require the knowledge of words**, in addition to the conclusion from previous research that ConvNets **do not require the knowledge about the syntactic or semantic structure of a language.** (Chinese News corpus convert to pinyin first, and then apply this model achieves only 10 something testing error.)

Dataset size forms a dichotomy between traditional and ConvNets models: the larger datasets tend to perform better.  

ConvNets may work well for user-generated data.  

---

#### Text Classification:

a.  Text classification could be used for NLP tasks, Information retrieval, Information filtering, spam email filtering,...

b.  Text Classification models: word vector and ConvNets

word vector: represent each word in the sentence with a vector, and all of these vector makes matrix, which represent the whole document/sentence.

c.  Concepts about CNN:

1d kernel, scale, padding, ...

https://github.com/ffflora/facial-expression-recognition-cv/blob/master/notes.md



#### The History of Text Classification:

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

---

### Model

Input: one-hot 

k-means vs LSTM

---

Q: This model is quite simple, why bother publish a paper?

A:  It is kind of easy to reproduce, and since it has done a lot of experiments on different datasets, it could be used as the comparative results for later or new model experiments.



Q: Disadvantages of this model?

A:  very deep - 9 layers; much params; have better results on larger datasets; not easy to train.



Q: Any other char-level model?

A: char-embedding 

---

#### Conclusion

This paper has provided with many comparative results with different models and datasets, including BOW and Deep learning models; the biggest achievement is that it offers a new method that is doing text classification based on character-level, instead of word vector, which is one of the most popular method nowadays. What worth to mention is that this model has a best or very comparative results on different datasets. 