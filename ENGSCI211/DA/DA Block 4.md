# DA Block 4
Qualitative (Categorical) variables

To set a categorical variable in R do as below:
```R
dataframe$variable = factor(dataframe$variable)

# to specify the ordering and baseline
dataframe$variable = factor(dataframe$variable, levels = c('category 1', 'category 2' ...))

# with number variables this would look like
dataframe$variable = factor(dataframe$variable, levels = c('2', '1', '3')) # reordered so 2 is baseline
```

R selects one of the categories as the baseline (usually in alphabetical order)

$$y = \beta_0 + \beta_2 x_2 + \beta_3 x_3 + \epsilon$$
Where $x_i$ are boolean values that are true if the observation is in the group $i$.
So the `intercept` is $\beta_0$ or our first group.
$\beta_i$ is the difference between $\beta_0$ and $\mu_i$

confidence intervals for the linear model show the confidence interval for the mean of the baseline group
AND how each of the other groups differ from the baseline group

#### Analysis of Variance

F-test
- $H_0: \mu_1 = \mu_2 = ... = \mu_n$
- $H_1$: not all the group means are the same

$\alpha_i = \mu_i - \mu$

`anova(dataframe)` does this test in R
`multipleComp(dataframe)` produces all possible combinations for each variable as a baseline
