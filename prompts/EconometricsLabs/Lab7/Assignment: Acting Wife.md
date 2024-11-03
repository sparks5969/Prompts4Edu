---
title: "Lab 7 - Acting Wife"
author: "Your Name Here"
date: "Date Here"
output: html_document
---

Lab 7: Acting Wife Exercise

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

##Load in packages
Download the following packages before running this code

```{r}
library(lmtest);library(sandwich);library(haven);library(dplyr);library(jtools);library(tidyverse);
```

#Load the Data
```{r}
acting_wife <- read_dta("directory here/acting_wife_data_set (4).dta")
```


Read this summary of the paper "Acting Wife" by Leonardo Bursztyn, Thomas Fujiwara, and Amanda Pallais. https://slate.com/news-and-politics/2016/12/men-still-arent-comfortable-with-ambitious-women.html 
What are the main findings from the Acting Wife paper?


Replicate the coefficients in Panel A of Table 4 (excluding the Kling, Leibman, Katz index). Use robust standard errors. You will need to create variables and run multiple bivariate regressions for this.
Hint: We want the effect of the public treatment on all the different dependent variables listed.

```{r}
#summary(lm(salary ~ public, data=subset(acting_wife,single_female == 1))) 

```



Do these results match up to what you read in the paper? 

Explain how you would test whether or not the "Public" treatment had a different effect on Single vs. Non-Single women using an interaction term.
Run this specification.

```{r}

```


Do any results change? Do they now match what you found in the paper? Do they match the writeup in Slate?

What specification are they running in the last row in Table 4? Replicate the results the p-values for salary and desired weekly hours of work.
Another hint: They’re comparing the effect of the public treatment on single women to the effect of the public treatment on everyone else.

```{r}

```

Read this article:
https://slate.com/technology/2013/07/statistics-and-psychology-multiple-comparisons-give-spurious-results.html 

In two sentences or less, explain Gelman's central concern about "researcher degrees of freedom."

Go back to the Acting wife data. Trying constructing an alternate coding of the "single variable" from the maritalstatus variable. Do the results in the first row of Table 4 remain significant and negative? Does the result for desired weekly hours of work in the last row remain significant? 
Relate your findings to the Andrew Gelman article above.
