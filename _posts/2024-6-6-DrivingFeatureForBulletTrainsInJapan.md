---
layout: post
title: "Analyzing Customer Satisfaction Driving Features for Bullet Trains in Japan"
description: "Feature Imporatance for Passenger Satisfaction of Bullet Trains in Japan"
categories: [classification, feature importance]
tags: [xgboost, cross-validation, hyper-parameter tuning]
---

## Project Overview

## Context

This problem statement is based on the Shinkansen Bullet Train in Japan, and passengers’ experience with that mode of travel. This machine-learning exercise aims to determine the relative importance of each parameter with regard to their contribution to the passengers’ overall travel experience. The dataset contains a random sample of individuals who travelled on this train. The on-time performance of the trains along with passenger information is published in a file named ‘Traveldata_train.csv’. These passengers were later asked to provide their feedback on various parameters related to the travel along with their overall experience. These collected details are made available in the survey report labelled ‘Surveydata_train.csv’.

The objective of this problem is to understand which parameters play an important role in swaying passenger feedback towards a positive scale.

## Actions and Result
The target feature is ‘Overall Experience’ as 0 (unsatisfied) and 1 (satisfied)
The number of input features are 24. These are ‘Gender’, ‘Customer_Type’, ‘Age’, ‘Type_Travel’, ‘Travel_Class’, ‘Travel_Distance’, ‘Departure_Delay_in_Mins’, ‘Arrival_Delay_in_Mins’, ‘Overall_Experience’, ‘Seat_Comfort’, ‘Seat_Class’, ‘Arrival_Time_Convenient’, ‘Catering’, ‘Platform_Location’, ‘Onboard_Wifi_Service’, ‘Onboard_Entertainment’, ‘Online_Support’, ‘Ease_of_Online_Booking’, ‘Onboard_Service’, ‘Legroom’, ‘Baggage_Handling’, ‘CheckIn_Service’, ‘Cleanliness’, ‘Online_Boarding’.
The number of observations used as a training set is around 94,379.
Two Classification models are used: Random Forest and XGBoost

## Key Definition

- Random Forest: An ensemble of multiple decision trees. Each tree is constructed using a random subset of the dataset and a random subset of features. The results of each tree is aggregated, for classification, by majority voting.

- XGBoost (eXtream Gradient Boosting): An ensemble model that builds trees sequentially, each new tree improves by learning from mistakes of the previous ones. Boosting combines multiple individual weak trees. After hundreads of iterations, weak learners are converted to strong learners. It is a supervised learning boosting algorithm that uses gradient descent.
