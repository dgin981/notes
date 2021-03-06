matrix $A$ with dimensions $n \times n$ will $n$ eigenpairs ($\lambda_i$, $\vec s_i$)

Eigenvalue $\lambda_i$
Eigenvector $\vec s_i$

These eigenpairs will satisfy the governing equation: 
$A \vec s_i = \lambda_i \vec s_i$

unit square = [0, 0, 1, 1; 0, 1, 0, 1]

$$(A - \lambda_iI)\vec s_i = 0$$
$$\det(A-\lambda I)=0$$

if matrix $A$ is symmetric ($A=A^T$) and  has distinct eigenpairs then a diagonal factorisation of $A$ exists:
$A=SDS^-1$
where $D$ is a diagonal matrix of eigenvalues, and $S$ is a non-singular eigenvector matrix. 

$S^-1 = S^T$