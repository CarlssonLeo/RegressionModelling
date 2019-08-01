---
title: "Quiz1"
author: "Leo Carlsson"
date: "8/1/2019"
output: 
  html_document: 
    keep_md: yes
---



## Question 1
x <- c(0.18, -1.54, 0.42, 0.95)
w <- c(2, 1, 3, 1)

Give the value of μ that minimizes the least squares equation

```r
x <- c(0.18, -1.54, 0.42, 0.95)
w <- c(2, 1, 3, 1)
sum(w * x) / sum(w)
```

```
## [1] 0.1471429
```

## Question 2
Consider dataset:
x <- c(0.8, 0.47, 0.51, 0.73, 0.36, 0.58, 0.57, 0.85, 0.44, 0.42)
y <- c(1.39, 0.72, 1.55, 0.48, 1.19, -1.59, 1.23, -0.65, 1.49, 0.05)

Fit the regression through the origin and get the slope treating y

as the outcome and x as the regressor. (Hint, do not center the data since we want regression through the origin, not through the means of the data.)

```r
x <- c(0.8, 0.47, 0.51, 0.73, 0.36, 0.58, 0.57, 0.85, 0.44, 0.42)
y <- c(1.39, 0.72, 1.55, 0.48, 1.19, -1.59, 1.23, -0.65, 1.49, 0.05)
lm(y~x-1)
```

```
## 
## Call:
## lm(formula = y ~ x - 1)
## 
## Coefficients:
##      x  
## 0.8263
```

## Question 3
Do \verb|data(mtcars)|data(mtcars) from the datasets package and fit the regression model with mpg as the outcome and weight as the predictor. Give the slope coefficient.

```r
data(mtcars)
lm(mpg~wt, data = mtcars)
```

```
## 
## Call:
## lm(formula = mpg ~ wt, data = mtcars)
## 
## Coefficients:
## (Intercept)           wt  
##      37.285       -5.344
```
## Question 4
Consider data with an outcome (Y) and a predictor (X). The standard deviation of the predictor is one half that of the outcome. The correlation between the two variables is .5. What value would the slope coefficient for the regression model with YY as the outcome and XX as the predictor?

```r
#1
```

## Question 5
Students were given two hard tests and scores were normalized to have empirical mean 0 and variance 1. The correlation between the scores on the two tests was 0.4. What would be the expected score on Quiz 2 for a student who had a normalized score of 1.5 on Quiz 1?

```r
1.5*0.4
```

```
## [1] 0.6
```

## Question 6
Data: 
x <- c(8.58, 10.46, 9.01, 9.64, 8.86)
What is the value of the first measurement if x were normalized (to have mean 0 and variance 1)?

```r
x <- c(8.58, 10.46, 9.01, 9.64, 8.86)
(x-mean(x))/sd(x)
```

```
## [1] -0.9718658  1.5310215 -0.3993969  0.4393366 -0.5990954
```

## Question 7
Consider the following data set (used above as well). What is the intercept for fitting the model with x as the predictor and y as the outcome?

x <- c(0.8, 0.47, 0.51, 0.73, 0.36, 0.58, 0.57, 0.85, 0.44, 0.42)
y <- c(1.39, 0.72, 1.55, 0.48, 1.19, -1.59, 1.23, -0.65, 1.49, 0.05)

```r
x <- c(0.8, 0.47, 0.51, 0.73, 0.36, 0.58, 0.57, 0.85, 0.44, 0.42)
y <- c(1.39, 0.72, 1.55, 0.48, 1.19, -1.59, 1.23, -0.65, 1.49, 0.05)
lm(y~x)
```

```
## 
## Call:
## lm(formula = y ~ x)
## 
## Coefficients:
## (Intercept)            x  
##       1.567       -1.713
```

## Question 8
You know that both the predictor and response have mean 0. What can be said about the intercept when you fit a linear regression?

```r
#Must be 0
```

## Question 9
What value minimizes the sum of the squared distances between these points and itself?
x <- c(0.8, 0.47, 0.51, 0.73, 0.36, 0.58, 0.57, 0.85, 0.44, 0.42)


```r
x <- c(0.8, 0.47, 0.51, 0.73, 0.36, 0.58, 0.57, 0.85, 0.44, 0.42)
mean(x)
```

```
## [1] 0.573
```

## Question 10
Let the slope having fit Y as the outcome and X as the predictor be denoted as \beta_1 β Let the slope from fitting X as the outcome and Y as the predictor be denoted as \gamma_1 γ 
Suppose that you divide \beta_1β by \gamma_1γ in other words consider \beta_1 / \gamma_1 β  /γ What is this ratio always equal to?


```r
#var(y)/var(x)
```

