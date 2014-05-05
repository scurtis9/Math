---
title       : Factor Analysis
subtitle    : 
author      : Shane Curtis
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
---

## What is Factor Analysis?

FA and PCA (principal components analysis) are methods of data reduction
> - Take many variables and explain them with a few “factors” or “components”
> - Correlated variables are grouped together and separated from other variables with low or no correlation




--- .class #id 

## What is FA?

1. Patterns of correlations are identified and either used as descriptives (PCA) or as indicative of underlying theory (FA)
2. Process of providing an operational definition for latent construct (through regression equation)

---

## FA vs. PCA: Conceptually

- FA produces factors; PCA produces components
- Factors cause variables; components are aggregates of the variables

---

## FA vs. PCA: Conceptually

<img src="/home/shane/FactorAnalysis/assets/img/FAPCA.jpeg" height="550" />

---

## FA vs. PCA: Conceptually

> - FA analyzes only the variance shared among the variables (common variance without error or unique variance); PCA analyzes all of the variance
> - FA: “What are the underlying processes that could produce these correlations?”; PCA: Just summarize empirical associations, very data driven

---

## General Steps to FA

1. Selecting and Measuring a set of variables in a given domain
2. Data screening in order to prepare the correlation matrix
3. Factor Extraction
4. Factor Rotation to increase interpretability 
5. Interpretation
6. Validation and Reliability of the measures

---

## What makes a "good factor"?

- Makes sense
- Easy to interpret
- Simple structure
- Lack of cross-loadings

---

## Problems with FA

- Unlike many of the analyses so far there is no statistical criterion to compare the linear combination to
- It has been consided more art than science
  - There are a number of extraction methods
  - There are a number of rotation methods: Orthogonal vs. Oblique
  - Number of factors to extract
  - Communality estimates

---

## Types of FA

Exploratory FA
> - Summarizing data by grouping correlated variables
> - Investigating sets of measured variables related to theoretical constructs
> - Usually done near the onset of research

---

## Types of FA

Confirmatory
> - More advanced technique
> - When factor structure is known or at least theorized
> - Testing generalization of factor structure to new data, etc.
> - This is tested through SEM methods

---

## Terminology

- Observed correlation matrix
- Reproduced correlation matrix
- Residual correlation matrix

---

## Terminology

Orthogonal Rotation
- Loading Matrix: correlation between each variable and the factor

Oblique Rotation
- Factor Correlation Matrix: correlation between the factors
- Structure Matrix: correlation between factors and variables
- Pattern Matrix: unique relationship between each factor and variable uncontaminated by overlap between the factors

---

## Terminology

- Factor Coefficient Matrix: coefficients used to calculate factor scores

--- .wrappre .centrepre .smaller


```
Factor Analysis using method =  pa
Call: fa(r = corMat, nfactors = 2, rotate = "oblimin", fm = "pa")
Standardized loadings (pattern matrix) based upon correlation matrix
       PA1   PA2   h2    u2 com
BIO   0.86  0.02 0.75 0.255 1.0
GEO   0.78  0.05 0.63 0.369 1.0
CHEM  0.87 -0.05 0.75 0.253 1.0
ALG  -0.04  0.81 0.65 0.354 1.0
CALC  0.01  0.96 0.92 0.081 1.0
STAT  0.13  0.50 0.29 0.709 1.1

                       PA1  PA2
SS loadings           2.14 1.84
Proportion Var        0.36 0.31
Cumulative Var        0.36 0.66
Proportion Explained  0.54 0.46
Cumulative Proportion 0.54 1.00

 With factor correlations of 
     PA1  PA2
PA1 1.00 0.21
PA2 0.21 1.00

Mean item complexity =  1
Test of the hypothesis that 2 factors are sufficient.

The degrees of freedom for the null model are  15  and the objective function was  2.87
The degrees of freedom for the model are 4  and the objective function was  0.01 

The root mean square of the residuals (RMSR) is  0.01 
The df corrected root mean square of the residuals is  0.02 

Fit based upon off diagonal values = 1
Measures of factor score adequacy             
                                                PA1  PA2
Correlation of scores with factors             0.94 0.96
Multiple R square of scores with factors       0.88 0.93
Minimum correlation of possible factor scores  0.77 0.86
```

