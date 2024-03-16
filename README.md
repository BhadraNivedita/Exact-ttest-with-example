# What is exact ttest? An example in R.

An exact test is a statistical test that provides an exact p-value without relying on large-sample approximations. These tests are particularly useful when sample sizes are small, making the assumptions of asymptotic tests (tests relying on large-sample approximations) potentially unreliable.

In the context of hypothesis testing, an exact test computes the probability of observing the test statistic under the null hypothesis exactly, without relying on asymptotic distributions. This is often done by considering all possible outcomes that are at least as extreme as the observed data and calculating the probability of obtaining these outcomes under the null hypothesis.

Exact tests are commonly used in situations where the assumptions of parametric tests (such as the t-test, chi-square test, etc.) may not be met, such as small sample sizes, non-normal distributions, or when dealing with categorical data.

One common type of exact test is the Fisher's exact test, which is used to test the association between two categorical variables in a contingency table when sample sizes are small.

In R, when you specify `exact = TRUE` in functions like `t.test()` or `chisq.test()`, it often indicates that an exact test should be performed rather than relying on asymptotic approximations.


#  Mann-Whitney U test

The Mann-Whitney U test, also known as the Mann-Whitney-Wilcoxon test or Wilcoxon rank-sum test, is a non-parametric statistical test used to compare two independent groups to determine whether their distributions are the same or if one tends to have larger values than the other.

Here's how it works:

1. **Ranking**: Combine the data from both groups and rank them from smallest to largest, disregarding which group they come from. Ties are handled by assigning the average rank to tied values.

2. **Calculating U statistic**: The U statistic is calculated by summing the ranks of the observations from one group. It represents the number of times a randomly selected observation from group 1 would have a lower rank than a randomly selected observation from group 2.

3. **Hypothesis testing**: The null hypothesis of the Mann-Whitney U test is that there is no difference between the two groups' distributions. The alternative hypothesis is that one group tends to have larger values than the other.

4. **P-value calculation**: The significance of the U statistic is determined through reference to the Mann-Whitney U distribution under the null hypothesis. The p-value indicates the probability of observing a U statistic as extreme as the one calculated from the data, assuming the null hypothesis is true.

The Mann-Whitney U test is commonly used when the assumptions of parametric tests like the t-test are violated, such as when the data are not normally distributed or when there are outliers. It's widely applicable in various fields, including biology, social sciences, and engineering, where comparing groups with ordinal or non-normally distributed data is common.
