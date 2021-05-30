# Bayesian Networks for Prognosis Modelling to predict Health Diseases


## Prognosis Modelling with Bayesian Networks

Prognosis simply means foreseeing, predicting, or estimating the probability or risk of future conditions; familiar examples
are weather and economic forecasts. In medicine, prognosis commonly relates to the probability or risk of an individual
developing a particular state of health (an outcome) over a specific time, based on his or her clinical and non-clinical profile.
Outcomes are often specific events, such as death or complications, but they may also be quantities, such as disease
progression, (changes in) pain, or quality of life.. Prognosis may be shaped by a patient’s age, sex, history, symptoms,
signs, and other test results. Moreover, prognostication in medicine is not limited to those who are ill. Healthcare
professionals, especially primary care doctors, regularly predict the future in healthy individuals


## Goals and Aims of the project

Implementation of a BN network on Framingham Heart Study dataset to

determine and visualize interactions between variables and to estimate conditional

probability.

```
Steps:
```
1. Structure learning procedure;
2. Model validation;
3. Queries and Probabilities on Network


## Dataset

**Demographic Risks** Male: 0 = Female; 1 = Male,Age at exam time.:Range 30-
,education:1 = Some High School; 2 = High School or GED; 3 = Some College or
Vocational School; 4

**Behavioral Risks** : CurrentSmoker - Current smoker or not CigsPerDay - Average
number of cigarettes smoked per day Medical experiments: BPMeds - Patient is
under blood pressure medication PrevalentStroke - Previously had a stroke or not
PrevalentHyp - Prevalent Hypertension or not Diabetes - Patient has diabetes or
not TotChol - Total Cholesterol Glucose - Glucose level 1

**Physical examination:** DiaBP - Diastolic blood pressure BMI - Body mass index
Heart - Rate Heart Rate SysBP - Symbolic blood pressure

**Prediction Label :** TenYearCHD- Predicting if someone will have 10 year risk of
coronary heart disease CHD


## Filling NAs with Median


## Directed acyclic graph

Show relationships between variables

Each variable can affect and cause is predecessors but it cannot be vice versa

There cannot be loop in the network


**_More the number of arcs:_**
•Pro: higher predictive accuracy.
•Cons: higher complexity in
interpreting the network.


## Conditional Independence

When two variables are independent from each other,but can have a common
child.

For example a kid height and A kid knowledge,both can be conditional
independent given a third variable (child) which is kid’s age

In order for the Bayesian network to model a probability distribution, it relies on the
important assumption: each variable is conditionally independent of its
non-descendants, given its parents.


## Whitelisting


## Hill Climbing Algorithm

Hc is Score-based algorithm,Each candidate DAG is assigned a network score
reflecting its goodness of fit, which the algorithm then attempts to maximise. Hill
climbing tries to delete and to reverse each arc in the current candidate DAG and
to add each possible arc that is not already present and that does not introduce
any cycles.The result with with the highest score is compared with current
candidate and if it has a better score then current candidate of DAG becomes the
new max.



## BootStrap and arcs Strength

•Data are bootstrapped (n = 500).

•For each bootstrap sample a network is learned.

•The arcs that have a frequency greater than 0.75 are included in the network in

output from the procedure.

Checking strength of nodes and arcs created by the HC algorithm by resampling
multiple times and finding if the network learned by HC is significant or not



## Cross Validation

Cross-validation is done to obtain unbiased estimates for model’s goodness of fit.
By comparing fitting techniques and the respective parameters.In K fold the data
is randomly partitioned into k subsets. Each subset is used in turn to validate the
model fitted on the remaining k - 1 subsets.


## Cross validation on the network to make sure the loss  function is as low as possible



## Conditional probability queries 
