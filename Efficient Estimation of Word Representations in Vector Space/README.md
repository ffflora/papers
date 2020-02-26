# Background Knowledge

Machine Learning

Calculus

Programming Skills: C++, PyTorch

#### Language Model:

`sentence = {x1,x2,....,xn}`

use frequency of the corpus instead of the probabilities:

`p(xi) = count(xi)/N` 

`p(xi-1,xi) = count(xi-1,xi)/N`  

Use conditional probability `p(xi|xi-1)`:

`p(xi|xi-1) = count(xi-1,xi)/count(xi)` 

Markov chain k-gram model

#### Sigmod 

#### Gradient Descent

#### Softmax

---

# Distributed Representation 

The origin of NLP deep learning: features.

#### One-hot representation

Easy to represent, but the problems are 

- More words, higher the dimension.
- There are no connections between the words.

#### Distributed representation

Use word embedding,  which usually doesn't have a high dimension, therefore could represent the relationship/connections between the words, easy to compute the similarity.

---

## word2vec

word2vec is a way to train the 

- unsupervised learning, no need to annotation
- 压缩 self-encoding, to reduce the dimension itself
- contextual semantics (结合上下文语义)

### word2vec evaluation

#### Intrinsic Evaluation

Compare the similarity between the words:

`sim(w1,w2) = cos(wvec1,wvec2)`

#### Analogy (词类比)

`cos(w1-w2 +w3, wvec4)`

example: 

`W('woman') - W('man') = W('aunt') - W('uncle')`

`W('woman') - W('man') = W('queen') - W('king')`

### Word Vectors

Applications:

- useful for **extrinsic word vectoe evaluation**, such as text classification.

- When apply to other NLP tasks, it acts like *semi-supervised*

- Translation
- Manifold 

# Theories of word2vec

### CBOW (Continuous Bag of Words)

Use the context to predict **the** word.

example: <u>I</u> <u>play</u> <u>basketball</u> <u>this</u> <u>afternoon</u>.

If I take out the `basketball` from the sentence, and use the rest of the words to predict the probability the word `basketball`.

Classifier: w(t) =>`basketball`

Word Matrix => 

- `w(t-2)` : I
- `w(t-1) `: play
- `w(t+1)` : this
- `w(t+2) `: afternoon

`p(Wt|Wt-2, Wt-1, Wt+1, Wt+2) `= ? 

### Skip-gram

Input => `basketball`

TODO: predict the words around the `basketball`

- `p(wt-1|wt)` = ?
- `p(wt-2|wt)` = ?
- `p(wt+1|wt)` = ?
- `p(wt+1|wt)` = ?



---

# Highlights of the paper

## 1.2 Previous Works

## SVD

Window based co-occurrence matrix 

![Window based co-occurrence matrix ](https://image.slidesharecdn.com/276ntstrb68zmgaigvia-signature-4919aae08f0ae9f3256efdc5cbdacac6c2a288ad9f47715bbefcb0ae9f95eb31-poli-170419184013/95/a-panorama-of-natural-language-processing-31-638.jpg?cb=1492627773)

dimension: `V*V ` (`row*column`)

need to do dimension reduction => `V*k, i.e., k = 300` (we can't do reduction on the rows of the matrix, since the rows represent the words in the sentence, and each word needs its own vector representation; but we can do the reduction on the columns, since not every word in the columns appear in the sentence.)

#### How to do the dimension reduction?

**UV decomposition.** => SVD 

## Model Architectures

It focus on distributed representations of words learned by NN instead of LDA. LDA costs too much on large datasets.

### 2.1 Feedforward NN Language Model (NNLM)

based on the (n-1) words upfront, to predict the probability of the nth word, and need to maximize the probability. 

`p(xi|xi-1,xi-2,....xi-n)`