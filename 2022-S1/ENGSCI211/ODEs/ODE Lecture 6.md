# Laplace Transform Part 2

#### Step and Delta Functions

Unit Step Function
![Unit Step Function](1646860011.png)

Shifted United Step Function
![](1646860239.png)

$$L\{u(t-a)\} = \frac{e^{-as}}{s}$$

Dirac Delta Function
$$ \int^{\epsilon}_{-\epsilon} \delta(t) \space dt = 1 $$

![](1646860784.png)
$$ L\{\delta(t-a)\} = e^{-as} $$

### Useful Laplace Theorems
Linearity, you can put multiplying constants out
$$ L\{af(t)\} = aL\{f(t)\} $$

Shift-in-$s$ Theorem
![](1646862001.png)

Shift-in-$t$ Theorem
$$ L\{u(t-a)f(t-a)\} = e^{-as}F(s) $$
$$ L^{-1}\{e^{-as}F(s)\} = u(t-a)f(t-a) $$

Convolution Theorem
![](1646863065.png)