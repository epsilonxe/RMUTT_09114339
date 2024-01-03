# Module 2
From Requirements to Collection


## Learning Objectives
### In this lesson you will learn about:
- Data requirements and data understanding.
- What occurs during data collection.
- How to apply data requirements and data collection to any data science problem.


## Data Requirements
![flowchart](figures/ds_methodology.png)


Data Requirements <br> >>> Cooking with data <<<
<!-- .element: class="textontop" -->
<!-- .slide: data-background-image="figures/cooking.gif" -->


### From requirements to collection
<div class="container">
<div class="col selected">

**Data Requirements**
- What are data requirements?

<img src='figures/whh.png' style="max-height: 300px;"/>

</div>
<div class="col">

**Data Collection**
- What occurs during data collection?

<img src='figures/data_collection.png' style="max-height: 300px;"/>
</div>
</div>


Case Study:<br> CHF Re-admission
<!-- .element: class="textontop" -->
<!-- .slide: data-background-image="figures/heart_beat.gif"  -->


<!-- .slide: data-background="var(--main-color)" -->
### Case Study:<br> Selecting the cohort
<div class="container">
<div class="col");>

- Define and select cohort
	- In-patient within health insurance provider's service area
	- Primary diagnosis of CHF in one year
	- Contiuous enrollment for at least 6 months prior to primary CHF admission
	- Disqualifying conditions
</div>
<div class="col">
<img src="figures/cohort.png">	
	
</div>
</div>


<!-- .slide: data-background="var(--main-color)" -->
### Case Study:<br> Defining the data
<div class="container">
<div class="col">

- Contents, formats, representations suitable for decision tree classifier
	- One record per petient with columns representign variables (*dependent variable and predictors*)
	- Content covering all aspects of each petient's clinical history
		- Transaction format
		- Transformations required
</div>
<div class="col" data-markdown style="font-size: 50%;">

| age | sex | amn. | diab. | bldprs. | creat. | CHF |
|------|------|----------|----------|------------|------------|-----|
| ...  |  ... | ... | ... | ... | ... | ... |
| 55  |  F  | 1 | 0 | 60/144 | 176 | 1 |
| 78  |  F  | 0 | 0 | 64/121 | 106 | 0 |
| 66  |  M  | 1 | 0 | 79/125 | 112 | 1 |
| 42  |  F  | 1 | 1 | 68/133 | 141 | 1 |
| 60  |  M  | 0 | 1 | 73/145 | 133 | 0 |
| ...  |  ... | ... | ... | ... | ... | ... |
</div>
</div>


## Data Collection
![flowchart](figures/ds_methodology.png)


<!-- .slide: data-background-image="figures/ingredients.gif" -->
Data Collection <br> >>> Ingredients? <<<
<!-- .element: class="textontop" -->


### From requirements to collection
<div class="container">
<div class="col">

**Data Requirements**
- What are data requirements?

<img src='figures/whh.png' style="max-height: 300px;"/>

</div>
<div class="col selected">

**Data Collection**
- What occurs during data collection?

<img src='figures/data_collection.png' style="max-height: 300px;"/>
</div>
</div>


<!-- .slide: data-background-image="figures/heart_beat.gif"  -->
Case Study:<br> CHF Re-admission
<!-- .element: class="textontop" -->


<!-- .slide: data-background="var(--main-color)" data-auto-animate -->
### Case Study:<br> Gathering available data
<img id="data_col" src="figures/clinic_data_collection.png">


<!-- .slide: data-background="var(--main-color)" data-auto-animate -->
### Case Study:<br> Gathering available data
<div class="container">
<div class="col">

- Available data sources
	- Cooperate data warehouse (single source of medial & claim, eligibility, provider and member information)
	- In-petient record system
	- Claim payment system
	- Disease management program information
</div>
<div class="col">
<img data-id="data_col" src="figures/clinic_data_collection.png">
</div>
</div>


<!-- .slide: data-background="var(--main-color)" data-auto-animate -->
### Case Study:<br> Deferring inaccessible data
<div class="container">
<div class="col">

- Data wanted but not available
	- Pharmaceutical records
	- Decide to defer
</div>
<div class="col">
<img data-id="data_col" src="figures/data_unavailable.png">
</div>
</div>


<!-- .slide: data-background="var(--main-color)" data-auto-animate -->
### Case Study:<br> Merging data

Eliminate redundant data

<img data-id="data_col" src="figures/merge_data.png">
</div>
</div>