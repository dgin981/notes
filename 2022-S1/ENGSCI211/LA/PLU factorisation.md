$PA=LU$
where
- $P$: permutation matrix
- $A$: matrix for which we find the PLU factorisation
- $L$: lower triangular matrix
- $U$: upper triangular matrix

PLU uses row subtraction and row swap
$r_1 \leftrightarrow r_2$

The Permutation Matrix is made by performing row swap operations on a identity matrix

$P^T = P^{-1}$

premultiplying $A$ by $P$ effectively swaps the rows in $A$ by how the rows were swapped in $P$

The permutation matrix is used to get rid of zeroes in the diagonal

A row subtraction is performed if the pivot is non-zero
- Perform the row subtraction operation on $U$
- Record the row subtraction multiplier in $L$
- Leave $P$ unchanged

A row swap is performed if the pivot is zero
- Perform the row swap operation on $U$
- Record a zero in L, swap previously evaluated elements of $L$ in the corresponding rows
- Perform the row swap operation on $P$

PLU factorisation simplifies to LU factorisation if $P=I$

