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

In addition to the core topic, there will be a (brief) discussion of a few additional topics:
1. Influential recent "breakthrough" papers applying machine learning (GPT-3, AlphaFold, etc), to get a sense of the "real" problems people want to solve.
2. Important recent papers in statistical learning theory; to set the a sense of progress on the theoretical foundations of the area.


The class will be based mainly on student presentations of papers. We imagine a critical discussion of one or two papers 
per lecture; and several contiguous lectures on the same theme. The goal will be to develop a deep understanding of recent research.

See also the syllabus: 

* [Syllabus](https://github.com/dobriban/Topics-In-Modern-Statistical-Learning/blob/master/Syllabus/stat-991-spring-2022-syllabus.pdf). 


## Influential recent ML papers
Why are people excited about ML?
* [Dermatologist–level classification of skin cancer with deep neural networks](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8382232/pdf/nihms-1724608.pdf)
* [Language Models are Few-Shot Learners](https://arxiv.org/abs/2005.14165)
* [Highly accurate protein structure prediction with AlphaFold](https://www.nature.com/articles/s41586-021-03819-2)
* [End to End Learning for Self-Driving Cars](https://arxiv.org/abs/1604.07316)

## Uncertainty quantification
Why do we need to quantify uncertainty? What are the main approaches?

### Calibration

* [The Comparison and Evaluation of Forecasters](https://www.jstor.org/stable/2987588)
* [Strictly proper scoring rules, prediction, and estimation](https://sites.stat.washington.edu/raftery/Research/PDF/Gneiting2007jasa.pdf)
* [Probabilistic forecasts, calibration and sharpness](https://sites.stat.washington.edu/people/raftery/Research/PDF/Gneiting2007jrssb.pdf)
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

### Conformal prediction++

* [Learning by Transduction](https://arxiv.org/abs/1301.7375)
* [A Tutorial on Conformal Prediction](https://www.jmlr.org/papers/v9/shafer08a.html)
* Book [Conformal Prediction for Reliable Machine Learning](https://www.sciencedirect.com/book/9780123985378/conformal-prediction-for-reliable-machine-learning)
* [Distribution-Free Predictive Inference For Regression](https://arxiv.org/abs/1604.04173)
* [Predictive inference with the jackknife+](https://arxiv.org/abs/1905.02928). * [Slides](https://github.com/dobriban/Topics-in-deep-learning/blob/master/Stat%20991%20presentations/Fall%202019/Slides/BarberSlides-whoa-psi-2019.pdf). 
* [Nested conformal prediction and quantile out-of-bag ensemble methods](https://arxiv.org/abs/1910.10562)
* [Exchangeability, Conformal Prediction, and Rank Tests](https://arxiv.org/abs/2005.06095)
* [Adaptive Conformal Inference Under Distribution Shift](https://arxiv.org/abs/2106.00170)

### Prediction sets

* [PAC Confidence Sets for Deep Neural Networks via Calibrated Prediction](https://arxiv.org/abs/2001.00106)
* [Distribution-Free, Risk-Controlling Prediction Sets](https://arxiv.org/abs/2101.02703)

### Classical statistical goals: confidence intervals, (single and multiple) hypothesis testing

* [Only Closed Testing Procedures are Admissible for Controlling False Discovery Proportions](https://arxiv.org/abs/1901.04885)
* [E-values: Calibration, combination, and applications](https://arxiv.org/pdf/1912.06116.pdf)
* [Universal Inference](https://arxiv.org/abs/1912.11436)
* [Permutation-based Feature Importance Test (PermFIT)](https://www.nature.com/articles/s41467-021-22756-2)

### OOD Detection

* [A Simple Unified Framework for Detecting Out-of-Distribution Samples and Adversarial Attacks](https://arxiv.org/abs/1807.03888)
* [Likelihood Ratios for Out-of-Distribution Detection](https://arxiv.org/abs/1906.02845)
* [Testing for Outliers with Conformal p-values](https://arxiv.org/abs/2104.08279)

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


## Learning theory & training methods

* [A Theory of Universal Learning](https://arxiv.org/abs/2011.04483)
* [Orthogonal Statistical Learning](https://arxiv.org/abs/1901.09036)
* [Unbiased Gradient Estimation in Unrolled Computation Graphs with Persistent Evolution Strategies](http://proceedings.mlr.press/v139/vicol21a.html)
* [Deep learning: a statistical viewpoint](https://arxiv.org/abs/2103.09177)


## Distributed learning

* [Optimal Complexity in Decentralized Training](https://arxiv.org/abs/2006.08085)
* [The Min-Max Complexity of Distributed Stochastic Convex Optimization with Intermittent Communication](https://arxiv.org/abs/2102.01583)

## Lectures

Lectures 1 and 2: Introduction. Presented by Edgar Dobriban. 

Lecture 3: ...

## Other materials

### Recent workshops and tutorials on related topics

* [ICML 2021 Workshop on Uncertainty & Robustness in Deep Learning](https://sites.google.com/view/udlworkshop2021/home)
* [Workshop on Distribution-Free Uncertainty Quantification at ICML 2021](https://sites.google.com/berkeley.edu/dfuq21)
* [NeurIPS 2020 Tutorial on Practical Uncertainty Estimation and Out-of-Distribution Robustness in Deep Learning](https://nips.cc/virtual/2020/public/tutorial_0f190e6e164eafe66f011073b4486975.html)

### Seminar series
* [International Seminar on Distribution-Free Statistics](https://sites.google.com/view/isdfs/home)

### Probability background
* Penn courses STAT 430, STAT 930.
* [Stat 110: Probability, Harvard](https://projects.iq.harvard.edu/stat110). * [edX course](https://www.edx.org/course/introduction-to-probability), * [book](http://probabilitybook.net/)
* [Online probability book](https://www.probabilitycourse.com/)

## ML background
* Penn courses CIS 520, ESE 546, [STAT 991](https://github.com/dobriban/Topics-in-deep-learning), and links therein

### Perspectives
* [Comments on AI, and the role of statistics by Candes, Duchi & Sabatti](https://statweb.stanford.edu/~candes/publications/downloads/Candes2019Comments.pdf)
* [Prediction, Estimation, and Attribution, by Bradley Efron](https://efron.ckirby.su.domains//papers/2019PredictEstimatAttribut.pdf)

### Software tools
* [Uncertainty Toolbox](https://github.com/uncertainty-toolbox/uncertainty-toolbox), [associated papers](https://github.com/uncertainty-toolbox/uncertainty-toolbox/blob/master/docs/paper_list.md#calibration-sharpness-and-recalibration-in-deep-learning)


