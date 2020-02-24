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