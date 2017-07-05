### Some Terminologies
* Decision Stump
  * Single-node decision tree

### Meta-Algorithms/ Ensemble methods
* Definition
  * Combining multiple classifiers
  * Using the same algorithms with different settings
  * Assigning different parts of the dataset to different classifiers

* Bagging/ Bootstrap aggregating
  * The data is taken from the original dataset S times to make S new datasets. The datasets are the same size as the original. Each dataset is built by randomly selecting an example from the original with replacement.  
  After the S datasets are built, a learning algorithm is applied to each one individually

### AdaBoost (Adaptive Boosting)
* Definition about boosting
  * In boosting, the different classifiers are trained sequentially. Each new classifier is trained based on the performance of those already trained. Boosting makes new classifiers focus on data that was previously misclassified by previous classifiers.  
  The output is calculated from a weighted sum of all classifiers.

* Theory
  * Initially, we need a week classifier. A weight is applied to every example in the training dataset.(**Called weight vector D**). Initially, these weights are equal and a week classifier is first trained on the training data. The errors from the week classifier are calculated. And the week classifier is trained a second time with the same dataset. After the second time, the weights of the training set are adjusted so the examples properly classified the first time are weighted less and the examples incorrectly classified the first time are weighted more.  
  To get one answer from all of these weak classifiers, AdaBoost assigns $\alpha$ values to each of the classifiers. The $\alpha$ values are based on the error of each weak classifier
  * Error
    * $\varepsilon = \frac{number of incorrectly classified examples}{total number of examples}$
  * Alpha
    * $\alpha = frac{1}{2} \ln{\frac{1 - \varepsilon}{\varepsilon}}$
