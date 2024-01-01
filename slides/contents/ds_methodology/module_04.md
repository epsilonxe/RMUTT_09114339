# Module 4
From Modeling to Evaluation


## Learning Objectives
### In this lesson you will learn about:
- What the purpose of data modeling is.
- Some characteristics of the modeling process.
- What it means to evaluate a model.
- Ways in which a model is evaluated.
- How to apply modeling and model evaluation to any data science problem.


## Modeling
![flowchart](figures/ds_methodology.png)


Modeling<br> >>> Sampling the food <<<
<!-- .element: class="textontop" -->
<!-- .slide: data-background-image="figures/cook_sampling.gif" -->


### From modeling to evaluation
<div class="container">
<div class="col selected">

**Modeling**
- In what way can the data be visualized to get the answer that is required?

<img src='figures/thinking.png' style="max-height: 300px;"/>

</div>
<div class="col">

**Evaluation**
- Does the model used really answer the initial question?
- Does it need to be adjusted?

<img src='figures/evaluation.png' style="max-height: 300px;"/>
</div>
</div>


### Analytics Approaches<br> 
![ ](figures/analytics.png)


### Machine Learning Models<br> 
<img src="figures/ml_types.png" style="max-width: 70%;">


Case Study:<br> CHF Re-admission
<!-- .element: class="textontop" -->
<!-- .slide: data-background-image="figures/heart_beat.gif"  -->


### Case Study:<br> Analyzing the models

Decission tree classification models

<div data-markdown style="font-size: 65%;">

| Model | Relative Cost | Overall Accuracy | Sensitivity | Specificity |
|-------|---------------|------------------|------------|-------------|
|  | (Y:N) | (% correct of Y & N) | (Y accuracy) | (N accuracy) |
|1 | 1:1 | 85% | 45% | 97% |
|2 | 9:1 | 49% | 97% | 35% |
|3 | 4:1 | 81% | 68% | 85% |
</div>


<!-- .slide: " data-auto-animate -->
## Evaluation
![flowchart](figures/ds_methodology.png)


<!-- .slide: data-background-image="figures/gordon.gif" -->
Evaluation
<!-- .element: class="textontop" -->


### From modeling to evaluation
<div class="container">
<div class="col">

**Modeling**
- In what way can the data be visualized to get the answer that is required?

<img src='figures/thinking.png' style="max-height: 300px;"/>

</div>
<div class="col selected">

**Evaluation**
- Does the model used really answer the initial question?
- Does it need to be adjusted?

<img src='figures/evaluation.png' style="max-height: 300px;"/>
</div>
</div>


### Model evaluation
<div class="container">
<div class="col">

**Phase 1: Diagnostic measures**
![](figures/roc.png)

</div>
<div class="col par-left">

**Phase 2: Statistical significance** 
![](figures/stat_sig.png)

</div>
</div>


<!-- .slide: data-background-image="figures/heart_beat.gif"  -->
Case Study:<br> CHF Re-admission
<!-- .element: class="textontop" -->


### Case Study:<br> Misclassification costs
<div data-markdown style="font-size: 65%;">

| Model | Relative Cost | TPR | Specificity | FPR |
|-------|---------------|------------------|------------|-------------|
|  | (Y:N) | (Sensitivity) | (N accuracy) | (1-Specificity) |
|1 | 1:1 | 0.45 | 0.97 | 0.03 |
|2 | 1.5:1 | 0.60 | 0.92 | 0.08 |
|3 | 4:1 | 0.68 | 0.85 | 0.15 |
|4 | 9:1 | 0.97 | 0.35 | 0.65 |
</div>


### Case Study: Using the ROC curve
<div class="container">
<div class="col par-left">

Receiver Operating Characteristic curve 
- Diagnostic tool for classification model evaluation
- Classification model performance
- True-Positive Rate (TPR) vs False-Poisve Rate (FPR)
- Optimal model at maximum seperation

</div>
<div class="col par-left">

![](figures/roc_sum.png)

</div>
</div>