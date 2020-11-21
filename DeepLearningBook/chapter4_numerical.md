1. What is conditioning?
- Conditioning refers to how rapidly a function changes w.r.t small changes in its inputs.

2. Why might function having poor conditioning be problematic for scientific computation?
- Because rounding errors in the inputs can result in large changes in the output.

3. Consider function $f(x) = A^{-1}x; A\in R^{n \times n}$  and $A$ has an eigen decomposition, what is its condition number?
- $max_{i,j}|\frac{\lambda_i}{\lambda_j}|$ , ratio of the magnitude of the largest and smallest eigenvalue.
- When this number is large, matrix inversion is particularly sensitive to error in the input

4. What does the deriviative of the function specify?
- It specifies how to scall a small change in the input in order to obtain the corresponding change in the output.

5. What can the second derivative can be used?
- To determine whether a critical point is a local maximum, minimum, saddle point

6. When $f'(x) = 0 \ and \  f''(x) > 0$, we can conclude that x is a local minimum
- When $f"(x) >0$, $f'(x)$ increases as we move to the right, decrease as we move to the left
- In other words, as we move right, the slope begins to point uphill to the right, and as we move left, the slope begins to point uphill to the left.

7. When $f'(x) = 0 \ and \  f''(x) < 0$, we can conclude that x is a local maximum.
8. When $f'(x) = 0 \ and \  f''(x) = 0$, we can't conclude, $x$ may be saddle point, or a part of a flat region.
9. When the Hessian has a poor condition number, gradient descent performs poorly. This is because in one direction, the derivative increases rapidly, while in another direction, it increases slowly. Gradient descent is unaware of this change in the derivative so it does not know that it needs to explore preferentially in the direction where the derivative remains negative for longer.
10. When f is a positive definite quadratic function, Newton’s method consists of applying equation $x^* = x^0 - H(f)(x^0)^{-1} \nabla_xf(x^0)$  once to jump to the minimum of the function directly.
11. When f is not truly quadratic but can be locally approximated as a positive definite quadratic, Newton’s method consists of applying equation $x^* = x^0 - H(f)(x^0)^{-1} \nabla_xf(x^0)$  multiple times.
12. Newton’s method is only appropriate when the nearby critical point is a minimum (all the eigenvaluesof the Hessian are positive), whereas gradient descent is not attracted to saddlepoints unless the gradient points toward them.
13. What is first-order optimization algorithms?
- Algorithms that use only the gradient.
- e.g: Gradient descent
14. What is second-order optimization algorithms?
- Algorithms that use also the Hessian matrix.
- e.g: Newton's method
15. What is a Lipschitz continuous function?
- A function $f$ whose rate of chagne is bounded by a **Lipschitz constant K**
- $\forall x, \forall y, |f(x) - f(y)| \le K||x - y||_2$ 
16. What does Lipschitz continous function help us?
- It allows us to quantify our assumption that a small change in the input made by an algorithm (e.g: gradient descent) will have a small change in the output.

17. Sometimes we wish not only to maximize or minimize a function $f(x)$ over all possible values of $x$. Instead we may wish to find the maximal or minimal value of $f(x)$ for values of $x$ in some set $S$. This is known as **constrained optimization**. Points $x$ that lie within the set $S$ are called **feasible points** in constrained optimization terminology.