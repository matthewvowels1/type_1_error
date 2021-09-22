# type_1_error

This repo contains a brief simulation demonstrating how model misspecification 'guarantees' statistical significance with enough data.

We start by generating some data according to a simple linear data generating process. The goal is to estimate the (null) effect x1 -> y. If we correctly specify the model, the type 1 error rate stays as expected. However, if we exclude one of the confounders, it rises sharply with sample size.

The ommision of the confounder is a type of structure misspecification but the problems can equally well occur from functional misspecifcation   (see https://arxiv.org/abs/2009.10025). For instance, if there was a part of the relatioship which was non-linear which we failed to account for, this will also lead to the same biased estimate of the effect size. And, if the effect size estimate is biased, then it will be non-zero (because we know the true value is zero). Thus, it is a natural consequence that as we collect more data, our confidence intervals shrink and we start excluding zero.

For this particular example, we only need around 750-800 samples to guarantee a false positive. 

This repo is an extension of the ideas presented in https://arxiv.org/abs/2009.10025 

### Vowels, M.J. (in press) Misspecification and unreliable interpretations in psychology and social science. Psychological Methods.

![alt text](https://github.com/matthewvowels1/type_1_error/blob/main/type_1_error_rate_misspecification.png)


![alt text](https://github.com/matthewvowels1/type_1_error/blob/main/effect_size_null_effect_misspecification.png)
