---
title       : Credit Risk Assessment Application
subtitle    : An Overview
author      : MANL
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [rCharts: libraries/nvd3]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

* The Credit Risk Assessement Application allows the user 
    + to perform a basic investigation of the determinants of credit default
    + to predict individual credit default status
* The application provides two tools:
    + an interactive rChart (for exploratory analysis)
    + random forest modelling for prediction of credit default status

--- .class #id 

## Data

* The German Credit Data set was originally provided by Professor Dr. Hofmann
* It is can be accessed through the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Statlog+%28German+Credit+Data%29)
* The application uses a modified version provided by Lantz (2013) and can be accessed [here](https://www.packtpub.com/books/content/support/13251)
* The data contains 1,000 observations and covers information on seventeen individual risk characteristics

--- .class #id

## Explorative Analysis

<iframe src=' assets/fig/nvd3plot2-1.html ' scrolling='no' frameBorder='0' seamless class='rChart nvd3 ' id=iframe- chart34183e001997 ></iframe> <style>iframe.rChart{ width: 100%; height: 400px;}</style>
The graph shows credit amount by purpose grouped by credit default status (yes/ no).

(I did not figure out how to use interactive rCharts using own data on RPubs. Hence, I used a built-in data.)

--- .class #id

## Random Forest

* Application offers an interface for training a random forest using k-fold cross-validation
* The user provides two inputs:
    + Percentage of total observations that should be used for training
    + Number of folds for cross-validation (restricted to 2-5 folds due to computational reasons
* Training and validation of the random forest model are performed using the *caret* and the *randomForest* package
* The user can input client data and predict whether the default status will be 'yes' or 'no' based on the model estimated before and the entered data

