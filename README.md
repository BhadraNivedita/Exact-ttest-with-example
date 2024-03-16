# What is exact ttest? An example in R.

An exact test is a statistical test that provides an exact p-value without relying on large-sample approximations. These tests are particularly useful when sample sizes are small, making the assumptions of asymptotic tests (tests relying on large-sample approximations) potentially unreliable.

In the context of hypothesis testing, an exact test computes the probability of observing the test statistic under the null hypothesis exactly, without relying on asymptotic distributions. This is often done by considering all possible outcomes that are at least as extreme as the observed data and calculating the probability of obtaining these outcomes under the null hypothesis.

Exact tests are commonly used in situations where the assumptions of parametric tests (such as the t-test, chi-square test, etc.) may not be met, such as small sample sizes, non-normal distributions, or when dealing with categorical data.

One common type of exact test is the Fisher's exact test, which is used to test the association between two categorical variables in a contingency table when sample sizes are small.

In R, when you specify `exact = TRUE` in functions like `t.test()` or `chisq.test()`, it often indicates that an exact test should be performed rather than relying on asymptotic approximations.
