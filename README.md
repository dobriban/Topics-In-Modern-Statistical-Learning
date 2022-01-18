# STAT 991: Topics In Modern Statistical Learning (UPenn, 2022 Spring)

This class surveys advanced topics in statistical learning based on student presentations. 

The core topic of the course is uncertainty quantification for machine learning methods.
While modern machine learning methods can have a high prediction accuracy in a variety of problems,
it is still challenging to properly quantify their uncertainty.
There has been a recent surge of work developing methods for this problem.
It is one of the fastest developing areas in contemporary statistics.
This course will survey a variety of different problems and approaches, such as
calibration, prediction intervals (and sets), conformal inference, OOD detection, etc.
We will discuss both empirically successful/popular methods as well as theoretically justified ones.
See below for a sample of papers.

In addition to the core topic, there may be a (brief) discussion of a few additional topics:
1. Influential recent "breakthrough" papers applying machine learning (GPT-3, AlphaFold, etc), to get a sense of the "real" problems people want to solve.
2. Important recent papers in statistical learning theory; to set the a sense of progress on the theoretical foundations of the area.


The class will be based mainly on student presentations of papers. We imagine a critical discussion of one or two papers 
per lecture; and several contiguous lectures on the same theme. The goal will be to develop a deep understanding of recent research.

See also the syllabus: 

* [Syllabus](https://github.com/dobriban/Topics-In-Modern-Statistical-Learning/blob/master/Syllabus/syllabus.pdf). 


## Influential recent ML papers
Why are people excited about ML?
* [Dermatologist–level classification of skin cancer with deep neural networks](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8382232/pdf/nihms-1724608.pdf)
* [Language Models are Few-Shot Learners](https://arxiv.org/abs/2005.14165)
* [Highly accurate protein structure prediction with AlphaFold](https://www.nature.com/articles/s41586-021-03819-2)
* [End to End Learning for Self-Driving Cars](https://arxiv.org/abs/1604.07316)

## Uncertainty quantification
Why do we need to quantify uncertainty? What are the main approaches?


### Conformal prediction++

* [Vovk et al.'s paper series, and books](http://alrw.net/)
  * [A Tutorial on Conformal Prediction](https://www.jmlr.org/papers/v9/shafer08a.html)
* [Takeuchi’s prediction regions and theory](https://www.amazon.com/Contributions-Theory-Mathematical-Statistics-Takeuchi-ebook/dp/B08435357M), and [old lecture notes](http://onlineprediction.net/uploads/790717-takeuchi-memo.pdf)
* [Inductive Conformal Prediction](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.4.7849&rep=rep1&type=pdf)
* (A few) Papers from CMU group
  * [Distribution-Free Prediction Sets](https://www.stat.cmu.edu/~ryantibs/statml/lectures/Lei-Robins-Wasserman.pdf)
  * [Distribution-free prediction bands for nonparametric regression](https://www.stat.cmu.edu/~ryantibs/statml/lectures/Lei-Wasserman.pdf)
  * [Distribution-Free Predictive Inference For Regression](https://arxiv.org/abs/1604.04173)
* Review emphasizing exchangeability: [Exchangeability, Conformal Prediction, and Rank Tests](https://arxiv.org/abs/2005.06095)
* [Predictive inference with the jackknife+](https://arxiv.org/abs/1905.02928). * [Slides](https://github.com/dobriban/Topics-in-deep-learning/blob/master/Stat%20991%20presentations/Fall%202019/Slides/BarberSlides-whoa-psi-2019.pdf). 
* [Nested conformal prediction and quantile out-of-bag ensemble methods](https://arxiv.org/abs/1910.10562)
* [Adaptive Conformal Inference Under Distribution Shift](https://arxiv.org/abs/2106.00170)
* X-Conditional validity: Already listed above: [Mondrian Confidence Machines](http://alrw.net/old/04.pdf) (also in Vovk'05 book), [Lei & Wasserman'14](https://www.stat.cmu.edu/~ryantibs/statml/lectures/Lei-Wasserman.pdf)
  * Y-conditional: [Classification with confidence](https://www.jstor.org/stable/43304686)
  * others: [equalized coverage](https://arxiv.org/abs/1908.05428)
* Applications to various statistical models
  * Causal estimands and Counterfactuals: [Chernozhukov et al, An Exact and Robust Conformal Inference Method for Counterfactual and Synthetic Controls](https://arxiv.org/abs/1712.09089), [Cattaneo et al](https://cattaneo.princeton.edu/papers/Cattaneo-Feng-Titiunik_2021_JASA.pdf), [Lei and Candes, Conformal Inference of Counterfactuals and Individual Treatment Effects](https://arxiv.org/abs/2006.06138)
  * Quantile regression: [Romano et al](https://arxiv.org/abs/1905.03222)
* Dependence
  * [Conformal prediction for dynamic time-series](https://arxiv.org/abs/2010.09107)
  * [Exact and robust conformal
inference methods for predictive machine learning with dependent data](http://proceedings.mlr.press/v75/chernozhukov18a.html)


### Tolerance Regions and Related Notions

* [Wilks's original paper, 1941](https://www.jstor.org/stable/2235627)
  * [Wald's multivariate extension, 1943](https://www.jstor.org/stable/2236001)
  * Tukey's paper series: [1](https://projecteuclid.org/journals/annals-of-mathematical-statistics/volume-16/issue-2/Non-Parametric-Estimation-I-Validation-of-Order-Statistics/10.1214/aoms/1177731119.full), [2](https://www.jstor.org/stable/2236230), [3](https://www.jstor.org/stable/2236053); Fraser & Wormleighton's extensions [1](https://projecteuclid.org/journals/annals-of-mathematical-statistics/volume-22/issue-2/Nonparametric-Estimation-IV/10.1214/aoms/1177729650.full)
* Books
  * David & Nagaraja: Order statistics, Sec 7.2 (short but good general intro)
  * Krishnamoorthy & Mathew: Statistical tolerance regions
* Connections between inductive conformal prediction, training set conditional validity, tolerance regions: 
  * [Conditional validity of inductive conformal predictors](https://arxiv.org/abs/1209.2673)
  * [PAC Confidence Sets for Deep Neural Networks via Calibrated Prediction](https://arxiv.org/abs/2001.00106)
  * [Distribution-Free, Risk-Controlling Prediction Sets](https://arxiv.org/abs/2101.02703)


### Calibration

* Classics
  * Sec 5.a of Robert Miller's monograph: [Statistical Prediction by Discriminant Analysis](https://link.springer.com/book/10.1007/978-1-940033-52-5) (1962). Calibration is called "validity" here.
  * [Calibration of Probabilities: The State of the Art to 1980](http://www.ccnss.org/ccn_2014/materials/pdf/sigman/callibration_probabilities_lichtenstein_fischoff_philips.pdf)
  * A.P. Dawid, [The Well-Calibrated Bayesian](http://fitelson.org/seminar/dawid.pdf)
  * DeGroot & Fienberg, [The Comparison and Evaluation of Forecasters](https://www.jstor.org/stable/2987588), 1983
  * On-line setting (some of it is non-probabilistic): 
    * Foster & Vohra (1998) [Asymptotic Calibration](https://repository.upenn.edu/cgi/viewcontent.cgi?article=1033&context=statistics_papers)
    * Vovk, V. and Shafer, G. (2005) [Good randomized sequential probability forecasting is always possible](https://pure.royalholloway.ac.uk/portal/files/889848/Vovk_-_Good_randomized.pdf). JRSS-B
  * Gneiting et al., [Probabilistic forecasts, calibration and sharpness](https://sites.stat.washington.edu/people/raftery/Research/PDF/Gneiting2007jrssb.pdf)
* Modern ML
  * [On Calibration of Modern Neural Networks](http://proceedings.mlr.press/v70/guo17a.html)
  * [Measuring Calibration in Deep Learning](https://arxiv.org/abs/1904.01685)
  * [Distribution-free binary classification: prediction sets, confidence intervals and calibration](https://arxiv.org/abs/2006.10564)
  * [Beyond Pinball Loss: Quantile Methods for Calibrated Uncertainty Quantification](https://arxiv.org/abs/2011.09588)
  * [Learn then Test: Calibrating Predictive Algorithms to Achieve Risk Control](https://arxiv.org/abs/2110.01052)

### Bayesian approaches, ensembles

* [Dropout as a Bayesian Approximation: Representing Model Uncertainty in Deep Learning](http://proceedings.mlr.press/v48/gal16.html); [Uncertainty in Deep Learning, Yarin Gal PhD Thesis](https://mlg.eng.cam.ac.uk/yarin/thesis/thesis.pdf)
* [What Uncertainties Do We Need in Bayesian Deep Learning for Computer Vision?](https://arxiv.org/abs/1703.04977)
* [Simple and Scalable Predictive Uncertainty Estimation using Deep Ensembles](https://arxiv.org/abs/1612.01474)
* [Can You Trust Your Model's Uncertainty. Evaluating Predictive Uncertainty Under Dataset Shift](https://arxiv.org/abs/1906.02530)
* [Bayesian Layers: A Module for Neural Network Uncertainty](https://proceedings.neurips.cc/paper/2019/file/154ff8944e6eac05d0675c95b5b8889d-Paper.pdf)

### OOD Detection

* [A Simple Unified Framework for Detecting Out-of-Distribution Samples and Adversarial Attacks](https://arxiv.org/abs/1807.03888)
* [Likelihood Ratios for Out-of-Distribution Detection](https://arxiv.org/abs/1906.02845)
* [Testing for Outliers with Conformal p-values](https://arxiv.org/abs/2104.08279)
* [Conformal Anomaly Detection on Spatio-Temporal Observations with Missing Data](https://arxiv.org/abs/2105.11886)

### Classical statistical goals: confidence intervals, (single and multiple) hypothesis testing

* [Hartigan '1969](https://www.jstor.org/stable/2286069)
* [E-values: Calibration, combination, and applications](https://arxiv.org/pdf/1912.06116.pdf)
* [Universal Inference](https://arxiv.org/abs/1912.11436)
* [Permutation-based Feature Importance Test (PermFIT)](https://www.nature.com/articles/s41467-021-22756-2)
* [Only Closed Testing Procedures are Admissible for Controlling False Discovery Proportions](https://arxiv.org/abs/1901.04885)


### Inductive biases
* [Combining Ensembles and Data Augmentation can Harm your Calibration](https://arxiv.org/abs/2010.09875)
* [AugMix: A Simple Data Processing Method to Improve Robustness and Uncertainty](https://arxiv.org/abs/1912.02781)

### Reviews, applications, etc

* [A review of uncertainty quantification in deep learning: Techniques, applications and challenges](https://www.sciencedirect.com/science/article/pii/S1566253521001081)
* [A Survey of Uncertainty in Deep Neural Networks](https://arxiv.org/abs/2107.03342)
* [Deeply uncertain: comparing methods of uncertainty quantification in deep learning algorithms](https://iopscience.iop.org/article/10.1088/2632-2153/aba6f3/meta)
* [Empirical Frequentist Coverage of Deep Learning Uncertainty Quantification Procedures](https://arxiv.org/abs/2010.03039)
* [Aleatoric and Epistemic Uncertainty in Machine Learning. An Introduction to Concepts and Methods](https://arxiv.org/abs/1910.09457)
* [Uncertainty Baselines. Benchmarks for Uncertainty and Robustness in Deep Learning](https://arxiv.org/abs/2106.04015)
* [A Gentle Introduction to Conformal Prediction and Distribution-Free Uncertainty Quantification](https://arxiv.org/abs/2107.07511)
* [Generalized OOD detection](https://github.com/Jingkang50/OODSurvey)
* [List of resources on conformal prediction](https://github.com/valeman/awesome-conformal-prediction)

### Classical statistical goals: confidence intervals, (single and multiple) hypothesis testing

* [Only Closed Testing Procedures are Admissible for Controlling False Discovery Proportions](https://arxiv.org/abs/1901.04885)
* [E-values: Calibration, combination, and applications](https://arxiv.org/pdf/1912.06116.pdf)
* [Universal Inference](https://arxiv.org/abs/1912.11436)
* [Permutation-based Feature Importance Test (PermFIT)](https://www.nature.com/articles/s41467-021-22756-2)


## Lectures

Lectures 1 and 2: Introduction. Presented by Edgar Dobriban. 

Lecture 3: ...

## Other topics

### Learning theory & training methods

* [A Theory of Universal Learning](https://arxiv.org/abs/2011.04483)
* [Orthogonal Statistical Learning](https://arxiv.org/abs/1901.09036)
* [Unbiased Gradient Estimation in Unrolled Computation Graphs with Persistent Evolution Strategies](http://proceedings.mlr.press/v139/vicol21a.html)
* [Deep learning: a statistical viewpoint](https://arxiv.org/abs/2103.09177)


### Distributed learning

* [Optimal Complexity in Decentralized Training](https://arxiv.org/abs/2006.08085)
* [The Min-Max Complexity of Distributed Stochastic Convex Optimization with Intermittent Communication](https://arxiv.org/abs/2102.01583)

## Other materials

### Recent workshops and tutorials on related topics

* [ICML 2021 Workshop on Uncertainty & Robustness in Deep Learning](https://sites.google.com/view/udlworkshop2021/home)
* [Workshop on Distribution-Free Uncertainty Quantification at ICML 2021](https://sites.google.com/berkeley.edu/dfuq21)
* [NeurIPS 2020 Tutorial on Practical Uncertainty Estimation and Out-of-Distribution Robustness in Deep Learning](https://nips.cc/virtual/2020/public/tutorial_0f190e6e164eafe66f011073b4486975.html)

### Seminar series
* [International Seminar on Distribution-Free Statistics](https://sites.google.com/view/isdfs/home)

### Software tools
* [Uncertainty Toolbox](https://github.com/uncertainty-toolbox/uncertainty-toolbox), [associated papers](https://github.com/uncertainty-toolbox/uncertainty-toolbox/blob/master/docs/paper_list.md#calibration-sharpness-and-recalibration-in-deep-learning)
* [Uncertainty Baselines](https://github.com/google/uncertainty-baselines/tree/main/baselines)
* [MAPIE](https://github.com/scikit-learn-contrib/MAPIE), conformal-type methods

### Probability background
* Penn courses STAT 430, STAT 930.
* [Stat 110: Probability, Harvard](https://projects.iq.harvard.edu/stat110). [edX course](https://www.edx.org/course/introduction-to-probability), [book](http://probabilitybook.net/)
* [Online probability book](https://www.probabilitycourse.com/)

### ML background
* Penn courses CIS 520, ESE 546, [STAT 991](https://github.com/dobriban/Topics-in-deep-learning), and links therein

### Perspectives
* [Comments on AI, and the role of statistics by Candes, Duchi & Sabatti](https://statweb.stanford.edu/~candes/publications/downloads/Candes2019Comments.pdf)
* [Prediction, Estimation, and Attribution, by Bradley Efron](https://efron.ckirby.su.domains//papers/2019PredictEstimatAttribut.pdf)



