# Numerical Methods
#### Jacobi

Rearrange each equation for a new solution variable
Equation 1 is rearranged for $x_1$ 
Equation 2 is rearranged for $x_2$
and so on...

where $k$ is the iteration number and $C_1$ and $C_2$ are constants from rearranging the equation
$x_n^{(k)} = C_1 + C_2x_m^{(k-1)}$
$x_m^{(k)} = C_3 + C_4x_n^{(k-1)}$

#### Gauss-Seidel

Newly estimated solution variables are used in the subsequent update equations
$x_n^{(k)} = C_1 + C_2x_m^{(k-1)}$
$x_{m}^{(k)} = C_3 + C_4x_n^{(k)}$

#### Matrix form

$$ \vec x^{(k)} = C \vec x^{(k-1)} + \vec d $$

For Gauss-Seidel you need to substitute the previously estimated values

#### Convergence vs Divergence

Diagonal dominance of the coefficient matrix $A$.

Strict: $$|a_{ii}| > \sum_{i \neq j}|a_{ij}|$$
Weak: $$|a_{ii}| = \sum_{i \neq j}|a_{ij}|$$
None: $$|a_{ii}| < \sum_{i \neq j}|a_{ij}|$$

- Strictly diagonally dominant: all rows strict
- Irreducibly diagonally dominant: all rows strict or weak *and* one row strict
- Not diagonally dominant: at least one row not strict or weak

If $A$ is strictly or irreducibly diagonally dominant, the Jacobi and Gauss-Seidel methods will converge towards a solution.

#### Convergence using Frobenius Norm

$$||C||= \sqrt{\sum_{i=1}^{n} \sum_{j=1}^{n} (c_{ij})^2 }$$
where $dim(C)=n \times n$
system will converge if $||C||<1$


