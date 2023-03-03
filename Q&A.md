# Questions you might have

All questions I present here are solely based on my personal experience in supervised machine learning (SML). Likewise, all answers I provide underwent only my personal method of scrutinizing SML sources. That is, the questions and answers I present are not peer-reviewed, not exhaustive, and not guaranteed to be 'correct'. I suggest to always be critical of every (SML related) answer and to always read at least from two separate sources. If you regard ChatGPT as a 'source', then I suggest to read at least from three different sources.

## Is SML a single method, like a t-Test?
No. Just like a t-Test is a single tool in the toolkit of the '[General Linear Model](https://sites.oxy.edu/lengyel/m150/textbook/stglm.html "GLM")' (GLM), SML is more of a toolkit ('[Mathematical Optimization](https://web.stanford.edu/group/sisl/k12/optimization/#!index.md "Mathematical Optimization")'), not a single tool.

## Is SML *always* comprised of exactly six steps?
I have seen blog posts that presented seven steps. Others might present five steps. However, this is not the point. The point is that the number of steps is relatively small and each single step is easily comprehensible. Therefore, being certain of this can be very useful. It can provide orientation, as opposed to feeling lost. It can also help to build and to maintain confidence. That is, although hundreds and thousands of methods can be used within the SML toolkit, there will still only be six steps within which a method is applied. The large number of methods (and options within a single method) is usually intimidating, especially to so-called newbies. Knowing the six general principles (steps) of SML means to know which steps exist, which step comes first, second and so on. It also means that everybody can be certain that nobody can take two steps at the exact same time, and that some steps can never be made, unless the preceding step has been finished. Lastly, no matter what specific method (or option) has been selected, it must be used in service of exactly one of the six steps at a given time. The same method might (theoretically) be used in different steps (which is usually confusing), but not at the exact same time, and most likely not with the exact same purpose.

## Does SML produce causal predictions?
No, mostly not. Causal predictions have to meet the same counterfactual criteria (all of them!) as causal inference methods. I recommend this source: 
Maldonado, G., & Cox, L. A. (2020). Causal reasoning in epidemiology: Philosophy and logic. *Global Epidemiology, 2*, 100020.

## Can SML be described in one easy sentence?
It's worth a try. SML means to check how well the data-based forecasting may work in a real-world setting.

## What does 'works well' mean?
How 'well forecasting works' is a problem on its own. There is no single 'thumbs up' or 'thumbs down' result available. In fact, there are quite many so-called performance measures available. Some can even make a very good impression, even though the forecasting does not work well, or does not work at all. The most prominent example is the performance measure 'accuracy' (the unweighted mean of the two performance measures sensitivity and specifity). When having a binary outcome (e.g., diagnosis no versus yes), where only very few cases have the diagnosis, e.g., less than 1% (let's say eating disorder in men), then the data is very imbalanced. If the forecasting always predicts 'no diagnosis', then it is correct in over 99% of all instances in the data. Even on average the forecasting will only be a little below 99%. Superficially, the forecasting would give the impression of being almost perfect, even though being totally useless.
