### Bayesian decision theory

* In a nutshell, it means choosing the decision with the highest probability
* If p1(x, y) > p2(x, y), then the class is 1
* If p2(x, y) > p1(x, y), then the class is 2

### Bayes' rule (To manipulate conditional probabilities)

* p(c|x) = [p(x|c) * p(c)] / p(x)

### Classifying with conditional probabilities
* What we really need to compare is $p(c_{1}|x, y)$ and $p(c_{2}|x, y)$
* Written in English, it means given a point identified as **x, y**, what is the probability it cam from class $c_1$? and what is the probability it came from class $c_2$?
* The problem is that the equation from our friend is $p(x, y|c_{1})$, which is not the same. But we can use Bayes' rule to switch things around, i.e. $p(c_{i}|x, y) = \frac{p(x, y|c_{i})p(c_{i})}{p(x, y)}$. With these definitions, we can define the Bayesian classification rule: 
  * If $p(c_{1}|x, y) > p(c_{2}|x, y)$, then the class is $c_{1}$
  * If $p(c_{1}|x, y) < p(c_{2}|x, y)$, then the class is $c_{2}$

### Assumptions we made when using naive bayes
