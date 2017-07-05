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
