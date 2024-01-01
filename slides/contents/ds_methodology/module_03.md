# Module 3
From Understanding to Preparation


## Learning Objectives
### In this lesson you will learn about:
- What it means to understand data.
- What it means to prepare or clean data.
- Ways in which data is prepared.
- How to apply data understanding and data preparation to any data science problem.


## Data Understanding
![flowchart](figures/ds_methodology.png)


Data Understanding
<!-- .element: class="textontop" -->
<!-- .slide: data-background-image="figures/tomato.gif" -->


### From understanding to preparation
<div class="container">
<div class="col selected">

**Data Understanding**
- What does it mean to "prepare" or "clean" data?

<img src='figures/exploring_data.png' style="max-height: 300px;"/>

</div>
<div class="col">

**Data Preparation**
- What are ways in which data is prepared?

<img src='figures/data_preparation.svg' style="max-height: 300px;"/>
</div>
</div>


Case Study:<br> CHF Re-admission
<!-- .element: class="textontop" -->
<!-- .slide: data-background-image="figures/heart_beat.gif"  -->


<!-- .slide: data-background="var(--bg-color)" -->
### Case Study:<br> Understanding the data
<div class="container">
<div class="col");>

- Descriptive statistics
	- Univariate statistics
	- Pairwise correlations
	- Histogram

$$ f(a) + \sum_{k=1}^{n}\frac{\mathrm{d}^k}{\mathrm{d}t^k}f(u(t)) + \int_{0}^{1} \frac{(1-t)^n}{n!}\frac{\mathrm{d}^{n+1}}{\mathrm{d}t^{n+1}} f(u(t)) \mathrm{d}t $$
<!-- .element: style="font-size: 50%" -->

</div>
<div class="col" data-markdown>

Histograms are a good way to understand how values or a variable are distributed, and what sorts of data preparation may be needed to make the variable more useful in a model.

<img src="figures/histogram.gif">	
	
</div>
</div>


<!-- .slide: data-background="var(--bg-color)" -->
### Case Study:<br> Looking at data quality
<div class="container">
<div class="col">

- Data quality
	- Missing values
	- Invalid or misleading values
</div>
<div class="col">
<img src="figures/missing_data.png">
<img src="figures/missing_data_2.png">
</div>
</div>


<!-- .slide: data-background="var(--bg-color)" data-auto-animate -->
### Case Study:<br> This is an iterative process
<div class="container">
<div class="col">

- Iterative data collection and understanding
	- Refined definition of "CHE Re-admission"
</div>
<div class="col">
<img src="figures/ds_methodology.png">
</div>
</div>


<!-- .slide: " data-auto-animate -->
## Data Preparation
![flowchart](figures/ds_methodology.png)


<!-- .slide: data-background-image="figures/orange_cleaning.gif" -->
Data Preparation <br> >>> Cleaning <<<
<!-- .element: class="textontop" -->


<!-- .slide: data-background-image="figures/onion_chop.gif" -->
Data Preparation <br> >>> Transform <<<
<!-- .element: class="textontop" -->


### From understanding to preparation
<div class="container">
<div class="col">

**Data Understanding**
- What does it mean to "prepare" or "clean" data?

<img src='figures/exploring_data.png' style="max-height: 300px;"/>

</div>
<div class="col selected">

**Data Preparation**
- What are ways in which data is prepared?

<img src='figures/data_preparation.svg' style="max-height: 300px;"/>
</div>
</div>


### Example of data cleaning

<div data-markdown style="font-size: 70%;">

| Name | Date | EXP | Location | Country |
|------|------|-----|-----|-------|
|John Doe | 20022012 | 22 | BKK | THA |
| Marry Jane | 2013-02-03 | 2 | BKK | TH |
| Henny Ozbourn | 30-Sep-12 | 15 | Bangkok | Thailand |
| Kelly, Tom | 2015 02 20 |   | B | Thai |
| Marry Jane | 2013-02-03 | 2 | BKK | TH |
</div>


### Using domian knowledge
<div class="container">
<div class="col">
<img data-id="data_col" src="figures/feature_engineering.png">
</div>
<div class="col par-left">

**Feature engineering** is the process of using domain knowledge if the data to to create features that make the machine learning algorithms work.

Feature engineering is critical when machine learning tools are being applied to analyze the data.
</div>
</div>


### Working with text analysis
<div class="container">
<div class="col">
<img data-id="data_col" src="figures/book_page.jpg">
</div>
<div class="col par-left">

When working with text, **text analysis** steps for coding the data are required to be able
to manipulate the data.

The text analysis is critical to ensure that the proper groupings are set, and that the
programming is not overlooking what is hidden within.
</div>
</div>


<!-- .slide: data-background-image="figures/heart_beat.gif"  -->
Case Study:<br> CHF Re-admission
<!-- .element: class="textontop" -->


### Case Study:<br> Defining CHF admission/readmission

![chf_admission](figures/chf_admission.svg)


### Case Study:<br> Aggregating records
<div class="container">
<div class="col">
<img data-id="data_col" src="figures/collage.png">
</div>
<div class="col par-left">

- Transaction records
	- Claims: professional provider, facility, pharmaceutical
	- Inpatien & outpetient records: diagnoses, procedures, prescriptions, etc.
	- Possibly thousands per petient, depending on clinical history
</div>
</div>


### Case Study:<br> Aggregating to patient level
<div class="container">
<div class="col">
<img src="figures/patient_er.png">
<img src="figures/health_records.jpg" style="max-width: 65%;">
</div>
<div class="col par-left">

- Roll up to 1 record per patient
- Create new columns representing the transaction
	- Outpatients visits/ Inpatients episodes: frequency, recency, diagnoses, length of stay, procedures, prescriptions
	- Comorbidities with CHF
</div>
</div>


### Case Study:<br> More or less data needed?
<div class="container">
<div class="col">
<img src="figures/reading.gif">
</div>
<div class="col par-left">

- Literature reviews of important factors for CHF readmission ![chf_papers](figures/medical_papers.jpg)
- Loop back to data collection stage and add additional data, if needed

</div>
</div>


### Case Study:<br> Completing the dataset
<div class="container">
<div class="col" style="background-color: var(--second-color); color: var(--bg-color)">

| age | sex  | diab. | bld. | ... | CHFR |
|------|------|----------|------------|------------|-----|
| ...  |  ... | ... | ... | ... | ... | ... |
| 55  |  F   | 0 | 144 | ... | N |
| 78  |  F   | 0 | 121 | ... | N |
| 66  |  M   | 0 | 125 | ... | Y |
| 42  |  F   | 1 | 133 | ... | Y |
| 60  |  M   | 1 | 145 | ... | N |
| 43  |  F   | 0 | 132 | ... | Y |
| 33  |  F   | 0 | 162 | ... | N |
| ...  |  ...   | ... | ... | ... | ... |
</div>
<div class="col par-left">

Merge all data into one table
- One record per patient
- Create new variables
- List of variables used in modeling
	- Target: **CHF readmission with 30 days (Yes/No)**, following discharge from CHF hospitalization
	- Measures: *gender, age, primary drug, ...*
	- Diagnosis flags (Y/N): *CHF, pneumonia, ...*

</div>
</div>


### Case Study:<br> Using training and testing sets
<div class="container">
<div class="col">

<img src="figures/training_set.png" style="display: block; margin-block: 0 -20px">
<img src="figures/testing_set.png">

</div>
<div class="col par-left selected" style="background-color: var(--accent-color);">

- Cohort: 2,343 patients
	- Randomly divied into traning and tesing sets: 70% / 30% split
- Training: 1,640 patients
- Testing: 703 patients

</div>
</div>