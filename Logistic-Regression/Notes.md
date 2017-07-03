### Regression
* Finding the best-fit line to a set of points

### Gradient ascent
* Definition
  * If we want to find the maximum point on a function, then the best way to move is in the direction of the gradient. In other words, gradient ascent algorithm helps us minimize the error between actual and predicted values. (Linear Algebra: Best-fit line)
* Terminology
  * Weights: Coefficients of our function
* Formula
  * $\nabla f(x, y) = \begin{matrix} \frac{\partial f(x, y)}{\partial x} \\\ \frac{\partial f(x, y)}{\partial y} \end{matrix}$
* Gradient ascent algorithm
  * $\mathbf{w} := \mathbf{w} + \alpha \nabla \mathbf{w}f(\mathbf{w})$

### Using gradient ascent to find the best parameters
* Pseudocode
  * ```
    Start with the weights all set to 1
    Repeat R number of times:
       Calculate the gradient of the entire dataset
       Update the weights vector by alpha * gradient
       Return the weights vector
    ```

### Stochastic gradient ascent
