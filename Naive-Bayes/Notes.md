### Bayesian decision theory
* In a nutshell, it means choosing the decision with the highest probability
* If p1(x, y) > p2(x, y), then the class is 1
* If p2(x, y) > p1(x, y), then the class is 2

### Bayes' rule (To manipulate conditional probabilities)
* $p(c|x) = \frac{p(x|c)p(c)}{p(x)}$
  * Probability of observing event c given that event x is true

### Classifying with conditional probabilities
* What we really need to compare is $p(c_{1}|x, y)$ and $p(c_{2}|x, y)$
* Written in English, it means given a point identified as **x, y**, what is the probability it cam from class $c_1$? and what is the probability it came from class $c_2$?
* The problem is that the equation from our friend is $p(x, y|c_{1})$, which is not the same. But we can use Bayes' rule to switch things around, i.e. $p(c_{i}|x, y) = \frac{p(x, y|c_{i})p(c_{i})}{p(x, y)}$. With these definitions, we can define the Bayesian classification rule: 
  * If $p(c_{1}|x, y) > p(c_{2}|x, y)$, then the class is $c_{1}$
  * If $p(c_{1}|x, y) < p(c_{2}|x, y)$, then the class is $c_{2}$
  * Alternative form
    * $p(c_{i}|\mathbf{w}) = \frac{p(\mathbf{w}|c_{i})p(c_{i})}{p(\mathbf{w})}$ and note that **w** means it is a vector

### Assumptions we made when using naive bayes
* Each features are independent
* Every feature is equally important

### Classifying text with Python
* Token
  * A token is any combination of characters. You can think of tokens as words, but we may use things that are not words such as URLs. We will reduce every piece of text to a vector of tokens where 1 represents the token existing in the document and 0 represents that it is not present 

### Naive Bayes classifier training function (Pseudocode)
  ```
  Count the number of documents in each class
  for every training document:
      for each class:
          if a token appears in the document -> increment the count for that token
          increment the count for tokens
      for each class:
          for each token:
              divide the token count by the total token count to get conditional probabilities
      return conditional probabilities for each class
  ```

### Modifying the classifier for real-world conditions
* $ln(a * b) = ln(a) + ln(b)$
  * We do this to avoid underflow problem
* How can we get $p(\mathbf{w}|c_{i})$?
  * If we expand **w** into individual features, we could write this as $p(w_{0}, w_{1}, w_{2}...w_{N}|c_{i})$. Our assumption that all the words were independently likely, and something called conditional independence, says we can calculate this probability as $p(w_{0}|c_{i})p(w_{1}|c_{i})...p(w_{N}|c_{i})$
