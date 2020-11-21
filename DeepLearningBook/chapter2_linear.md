1. Why Squared $L_2$ norm is popular than normal $L_2$ norm?
 - Because:
     - Sqrt is complex to compute
     - Deriviates of the squared $L_2$ w.r.t each element of $x$ each depend only on the corresponding $x$. while $L_2$ depends on the entire vector.

2. Why in some context, Squared $L_2$ norm may be undesirable?
- Because it increases very slowly near the origin.
- In several ML applications, it's important to discriminate between elements that are exactly zero and elements that are small but nonzero

3. In case  when the difference between zero and nonzero elements is very important, what norm do we use?

- $L_1$: since it grows the same rate at all locations

4. What is reciprocal? Nghịch đảo
5. What is the gist of PCA?

- For each point $x^i \in R^n$ we'll find the corresponding code vector $c^i \in R^l$ 
- Encoding function $f(x) = c$ and decoding function $x \approx g(f(x))$ 
- Let $g(c) = Dc; D\in R^{n \times l}$ . $D$ 's columns are orthonormal.
- To find optimal $c$, we can use $L^2$ norm: $c^{*} = argmin_c||x - g(c)||_2$ 
- Square it then solve, we find $c = D^T x$  
- Encoding: $f(x) = D^T x$ , Decoding: $g(x) = DD^T x$ 
- How to find D?
    - Use Frobenius norm: $D^{*} = argmin_D \sqrt{\sum_{i,j}(x^i_j - r(x^i)_j)^2}$ , with $D^TD = I_l$ 
    - Then depends on how many principle components you want, solve for $l=...$ 

6. When we wish to recover a basis of principal components, the matrix $D$ is given by the $l$ eigenvectors corresponding to the largest eigenvalues.

