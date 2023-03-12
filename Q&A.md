# SML questions you might have

All questions I present here are solely based on my personal experience in supervised machine learning (SML). Likewise, all answers I provide underwent only my personal method of scrutinizing SML sources. That is, the questions and answers I present are not peer-reviewed, not exhaustive, and not guaranteed to be 'correct'. I suggest to always be critical of every (SML related) answer and to always read at least from two separate sources. If you regard ChatGPT as a 'source', then I suggest to read at least from three different sources.

## Is SML a single method, like a t-Test?
No. Just like a t-Test is a single tool in the toolkit of the '[General Linear Model](https://sites.oxy.edu/lengyel/m150/textbook/stglm.html "GLM")' (GLM), SML is more of a toolkit ('[Mathematical Optimization](https://www.britannica.com/science/optimization "Mathematical Optimization")'), not a single tool.

## Is SML *always* comprised of exactly six steps?
I have seen blog posts that presented seven steps. Others might present five steps. However, this is not the point. The point is that the number of steps is relatively small and each single step is easily comprehensible. Therefore, being certain of this can be very useful. It can provide orientation, as opposed to feeling lost. It can also help to build and to maintain confidence. That is, although hundreds and thousands of methods can be used within the SML toolkit, there will still only be six steps within which a method is applied. The large number of methods (and options within a single method) is usually intimidating, especially to so-called newbies. Knowing the six general principles (steps) of SML means to know which steps exist, which step comes first, second and so on. It also means that everybody can be certain that nobody can take two steps at the exact same time, and that some steps can never be made, unless the preceding step has been finished. Lastly, no matter what specific method (or option) has been selected, it must be used in service of exactly one of the six steps at a given time. The same method might (theoretically) be used in different steps (which is usually confusing), but not at the exact same time, and most likely not with the exact same purpose.

## Does SML produce causal predictions?
No, mostly not. Causal predictions have to meet the same counterfactual criteria (all of them!) as causal inference methods. I recommend this source: 
Maldonado, G., & Cox, L. A. (2020). Causal reasoning in epidemiology: Philosophy and logic. *Global Epidemiology, 2*, 100020.

## Can SML be described in one easy sentence?
It's worth a try. SML means to check how well the data-based forecasting may work in a real-world setting.

## What does 'works well' mean?
How 'well forecasting works' is a problem on its own. There is no single 'thumbs up' or 'thumbs down' result available. In fact, there are quite many so-called performance measures available. Some can even make a very good impression, even though the forecasting does not work well, or does not work at all. The most prominent example is the performance measure 'accuracy' (sum of true positives and true negatives in relation to all predictions). When having a binary outcome (e.g., diagnosis no versus yes), where only very few cases have the diagnosis, e.g., less than 1% (let's say eating disorder in men), then the data is strongly imbalanced. If the forecasting always predicts 'no diagnosis', then it is correct in over 99% of all instances in the data. Superficially, the forecasting would give the impression of almost perfect accuracy (because the sum of true positives and true negatives is almost completely (> 99%) dominated by the true negatives), even though being totally useless (the forecasting algorithm permanently 'predicts' negative).

## How many performance measures are there?
A lot. For starters, I recommend these sources:

Steyerberg, E. W., Vickers, A. J., Cook, N. R., Gerds, T., Gonen, M., Obuchowski, N., ... & Kattan, M. W. (2010). Assessing the performance of prediction models: a framework for some traditional and novel measures. *Epidemiology (Cambridge, Mass.), 21(1)*, 128.

Van Geloven, N., Giardiello, D., Bonneville, E. F., Teece, L., Ramspek, C. L., Van Smeden, M., ... & Steyerberg, E. (2022). Validation of prediction models in the presence of competing risks: a guide through modern methods. *bmj*, 377. DOI: 10.1136/bmj-2021-069249.

## Is there one single best performance measure?
Certainly not.

## Why are there *a lot* of performance measures?
Probably so that the elephant can be looked at from any possible angle?

## What is the best angle from which to look at the prediction performance?
It mostly depends on your specific research question. For instance, if a research question shall be answered by using SML, this almost always puts the focus on how accurate the outcome can be predicted **on the individual level**. It may therefore be surprising (at least to me it was) that the most commonly used performance measure, i.e., the so-called area under the receiver operating characteristic curve (short: AUROC or just AUC), is a summary performance measure (it summarizes performance across all individuals, and the way it summarizes it is very crude). It may also be surprising that performance evaluations that approach **the individual level**, i.e., calibration measures (Huang et al., 2020) are rarely presented in research papers that employ SML. One paper called calibration the Achilles heel of predictive analytics (Van Calster et al., 2019). Surprises like these, a paper by Altman and Royston (2000), and the fun in breaking a 'rule' (never have two opposing y-axes with different scales in the same plot), gave me the idea to develop the [predictMe](https://cran.r-project.org/web/packages/predictMe/vignettes/predictMe.html "predictMe") R package ([predictMe CRAN Download](https://cran.r-project.org/web/packages/predictMe/index.html "predictMe")). It can be used to visualize how far from perfect an individual prediction is, i.e., how accurate the prediction model is calibrated **on the individual level**.

Altman, D. G., & Royston, P. (2000). What do we mean by validating a prognostic model?. *Statistics in medicine, 19(4)*, 453-473.

Huang, Y., Li, W., Macheret, F., Gabriel, R. A., & Ohno-Machado, L. (2020). A tutorial on calibration measurements and calibration models for clinical prediction models. *Journal of the American Medical Informatics Association, 27(4)*, 621-633.

Van Calster, B., McLernon, D. J., Van Smeden, M., Wynants, L., Steyerberg, E. W., & Topic Group ‘Evaluating diagnostic tests and prediction models’ of the STRATOS initiative. (2019). Calibration: the Achilles heel of predictive analytics. *BMC medicine, 17*, 1-7.

## Is SML really worth the time and effort for psychologists?
I invested quite much time and effort and I am a psychologist. Therefore, of course I say yes. However, my 'yes' requires a specification. My time and effort included reading about how 'the father' of modern statistical learning Sir Ronald Fisher (1890-1962) provided the fundamental solid ground of the maximum likelihood principle (Edwards, 1974; Stigler, 2007), which we use every time we statistically estimate an hypothesized effect, because we approximately always use a statistical test that belongs to the [GLM](https://sites.oxy.edu/lengyel/m150/textbook/stglm.html "GLM") (see first question, top of this page). This is very noteworthy, because there are several review articles in (clinical) psychology and medicine (Christodoulou et al., 2019; Nusinovici et al., 2020) that have repeatedly shown that machine learning algorithms (modern optimization techniques) do not outperform logistic regression (the 'old' maximum likelihood optimization technique), at least not in the way that SML proponents expected it. However, even if this should not change, SML is very useful. The use is that it reveals a particular weakness of how empirical research has been and still is conducted in (clinical) psychology. That is, research results are not empirically cross-validated. They are narratively cross-validated (narrative comparison of associations across studies and narrative suggestions of possible reasons for concurrent and divergent results). Meta-analyses represent a limited and indirect step towards empirical cross-validation (Savitz & Forastiere, 2021; Metelli & Chaimani, 2020; Brooke et al., 2021; Borenstein, 2022).

Direct empirical cross-validation is *the* backbone of SML (see steps 2-6 on the poster). It shall prevent overconfidence in the result of the statistical prediction model. Inferential statistics in psychology at some point in history abandoned direct empirical cross-validation (de Rooij & Weeda, 2020). SML, in a way, brings it back. There are also other (hopefully) positive side effects of SML, e.g., being confronted with very important 'details' which the most widely used statistical methods ignore, first and foremost measurement error biases (Jacobucci & Grimm, 2020). What do I mean by 'ignore'? Regression analyses are practically ubiquitous in (clinical) psychology research. One 'detail' of this data analysis technique is the assumption that all variables in the model are measured without error.

Borenstein, M. (2022). In a meta-analysis, the I-squared statistic does not tell us how much the effect size varies. *Journal of Clinical Epidemiology, 152*, 281-284.

Brooke, B. S., Schwartz, T. A., & Pawlik, T. M. (2021). MOOSE reporting guidelines for meta-analyses of observational studies. *JAMA surgery, 156(8)*, 787-788.

Christodoulou, E., Ma, J., Collins, G. S., Steyerberg, E. W., Verbakel, J. Y., & Van Calster, B. (2019). A systematic review shows no performance benefit of machine learning over logistic regression for clinical prediction models. *Journal of clinical epidemiology, 110*, 12-22.

de Rooij, M., & Weeda, W. (2020). Cross-validation: A method every psychologist should know. *Advances in Methods and Practices in Psychological Science, 3(2)*, 248-263.

Edwards, A. W. (1974). The history of likelihood. *International Statistical Review/Revue Internationale de Statistique*, 9-15.

Jacobucci, R., & Grimm, K. J. (2020). Machine learning and psychological research: The unexplored effect of measurement. *Perspectives on Psychological Science, 15(3)*, 809-816.

Metelli, S., & Chaimani, A. (2020). Challenges in meta-analyses with observational studies. *BMJ Ment Health, 23(2)*, 83-87.

Nusinovici, S., Tham, Y. C., Yan, M. Y. C., Ting, D. S. W., Li, J., Sabanayagam, C., ... & Cheng, C. Y. (2020). Logistic regression was as good as machine learning for predicting major chronic diseases. *Journal of clinical epidemiology, 122*, 56-69.

Savitz, D. A., & Forastiere, F. (2021). Do pooled estimates from meta-analyses of observational epidemiology studies contribute to causal inference?. *Occupational and environmental medicine, 78(9)*, 621-622.

Stigler, S. M. (2007). The epic story of maximum likelihood. *Statistical Science*, 598-620.

## What is resampling in SML?
In order to simulate what might have happened if a developed prediction model had been applied to a new individual (or new individuals) in the real world, a single dataset must be split into at least two different subsets: The subset that serves to develop the prediction model and the subset that serves as the 'simulated' real-world individual(s), which are supposed to benefit from the prediction model. The proclaimed benefit consists of an improved decision-making for the individual(s), compared to making a decision that is not based on an empirically developed prediction model. Remember that this is the ultimate aim of SML research: For a certain outcome, the best possible algorithm shall one day be implemented in routine daily practice, predicting, for instance, whether a therapist's patient is going to attempt suicide in the future. If the therapist and/or the patient accepts the data-based estimation of increased risk, they would decide to intervene.

## Why is resampling done in SML?
Resampling is done to simulate the real-world situation. That is, in order to consider the implementation of algorithmic decision support in real-world practice, it first must be empirically shown how well the result of such an implementation might have been, had the algorithm already been deployed to the real world. Resampling is the only way to simulate this. The best possible SML research situation would be to have comparable independent datasets, e.g., from a multicenter study. One of the datasets would be used for tuning and training (see steps 3 and 4 on the poster), another one for testing (see step 5 on the poster), and yet another one for validating (see step 6 on the poster). This way the datasets would naturally be split from the beginning. However, very often the researcher only has got one (hopefully) big dataset which s/he must split up to simulate a real-world prediction situation.

## What is (hyperparameter) tuning in SML?
First, tuning. What is it? Tuning = A human being actively uses at least one of a number of options that a piece of machinery provides, in order for that piece of machinery to produce a better final result, compared to not having actively used the provided option(s). An everyday example is a digital camera (piece of machinery). To get a good final result (nice picture) when it is dark, the user actively uses the night mode of the camera (= several particular parameters, which are preset in the camera's software, are collectively selected by the photographer; note that these parameters are set very differently in the daylight mode). The point is, the user selects either a collection of parameters (or just a single parameter) of that piece of machinery, dependent on the current circumstance (e.g., night, darkness), a) in order to get as good as possible a final result, and b) BEFORE that piece of machinery is going to do its actual business (produce the picture; final result). This last point emphasizes that 'hyperparameters' are never 'obtained' or 'estimated' by a data model (= piece of machinery). They are actively selected by the researcher, BEFORE the data model starts to compute the estimations, e.g., regression weights and intercept.

Beware: Confusion may be caused by terminology. Hyperparameters sound similar to model parameters. They are very different things, see explanation above.

Recommended reading on hyperparamters:

Bischl, B., Binder, M., Lang, M., Pielok, T., Richter, J., Coors, S., ... & Lindauer, M. (2021). Hyperparameter optimization: Foundations, algorithms, best practices, and open challenges. *Wiley Interdisciplinary Reviews: Data Mining and Knowledge Discovery*, e1484.
