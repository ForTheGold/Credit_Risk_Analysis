# Credit_Risk_Analysis

An analysis of credit risk

## Overview

People all over the world use loans to do things such as purchase houses and cars as well as go to university.  Loans produce an opportunity as well as a challenge for banks in that they can make a great deal of money off the interest gathered on loans, but there is always a risk that the money will not be returned leading to losses for the banks.

Banks have traditionally relied on credit scores, income and collateral assets to assess lending risk, but the rise of FinTech has been able to automate the process using machine learning.  We have used several different machine learning models in order to assess the risk of loan applicants in order to find the best one.

## Results

Naive Random Oversampling



As you can see, we did not achieve a terrible score here, but it is not really that great either.  Only about 65% of our predictions will be correct.  Our main problem is that we have classified far too many loan applicants as low risk when they are in fact high risk.  We have nearly 7000 false negatives.  We can see that our precision is extremely low with finding high risk applicants.

SMOTE Oversampling



This method gave us nearly the same results with about 66% accuracy.  It has the same issue of identifying far too many loan applicants that are high risk as low risk.  Here there are over 5000 false negatives leading to a low precision and f1 score for that category.

Undersampling


Undersampling has produced an even worse result with only 54% of the applications being identified correctly.  The problem is the same that we have a huge number of false negatives.  This time the number is over 10,000 which is excessive.  This also leaves us with a low precision and f1 score for the high risk category.

Combination Sampling



We have the same problem with Combination sampling.  This method is about 64% accurate with a huge number of false negatives at over 7000.  This again leads to low precision and f1 scores.

Balanced Random Forest Classifier



This model is much improved with an accuracy of about 74%.  There are still many false negatives, but it is a great deal less at just over 2000.  Our precision and accuracy scores for the category have increased dramatically.

Easy Ensemble Adaboost Classifier



This is by far the best classifier at 93% accuracy.  The model has classified less than 1000 of the applicants as high risk incorrectly which leads to a great deal of improvement in our precision and f1 scores.

## Summary

We did not seem to get the best results with either over or undersampling.  Some of the methods may be used, but we have been able to find a few alternatives that produce better results.  By far the best result came from the easy ensemble adaboost classifier which returned an accuracy score of 93%.  That is a pretty good result.  Another alternative would be the balanced random forest classifier which came in a bit lower at 74%.

## Technologies

Scikit-learn
Imbalanced-learn
Pandas
NumPy
Python
Machine Learning