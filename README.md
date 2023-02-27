# posterSML

The poster is to be presented at the International Convention of Psychological Science (ICPS) 9th - 11th March 2023. The poster will be presented on Thursday, 9th March (11:45 - 12:45 h) at Panoramic Hall (Location: SQUARE - Brussels Convention Centre), board number is TI-11.

# FAQs you might have

All questions I present here are solely based on my personal experience in supervised machine learning (SML). Likewise, all answers I provide underwent only my personal method of scrutinizing information. That is, the FAQs and answers I present are not peer-reviewed, not exhaustive, and not guaranteed to be correct. I suggest to always be critical of every (SML related) answer and to always read at least from two separate sources.

## Is SML a single method?
No. SML is a single framework, which is comprised of six steps. I have seen blog posts that presented seven steps. Others might present five steps. However, this is not the point. The point is that the number of steps is relatively small and each single step is easily comprehensible. Therefore, this knowledge can be used for orientation purposes. It can also be used to build and to maintain confidence. That is, although hundreds and thousands of methods can be used within the SML framework, there will still only be six steps within which a method is applied. The number of methods and options can and usually it is intimidating, especially to so-called newbies. Knowing the six general principles (steps) of SML means to know which steps exist, which step comes first, second and so on. It also means that nobody can take two steps at the exact same time, and that certain steps can never be made, unless the preceding step has been finished. Lastly, no matter what specific method or option has been selected, it must be used in service of one of the six steps at a given time. The same method might (theoretically) be used in different steps, but again, not at the exact same time, and most likely not with the exact same purpose.

## Does SML produce causal predictions?
No, mostly not. Causal predictions have to meet the same counterfactual criteria (all of them!) as causal inference methods. I recommend this source: 
Maldonado, G., & Cox, L. A. (2020). Causal reasoning in epidemiology: Philosophy and logic. Global Epidemiology, 2, 100020.

## Can SML be described in one easy sentence?
Who does not want to understand something right away? SML means to check how well the data-based forecasting may work in a real-world setting. However, what 'how well it works' is a problem on its own, because there is not single 'thumbs up' result. In fact, there are quite many so-called performance results available. Some may make a good impression, even though the forecasting does not work well at all. The most prominent example is the performance measure 'accuracy'. When having a binary outcome (diagnosis x no versus yes) and only very few cases with the diagnosis, e.g., less than 1%, the data is very imbalanced. If the forecasting always predicts 'no diagnosis x', then it is correct in over 99% of all instances in the data. On average, the forecasting will be only be a little below 99%. Superficially, the forecasting would make an almost perfect impression.

