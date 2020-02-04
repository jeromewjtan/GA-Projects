# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) 

# Project 4: West Nile Virus Prediction

### Context and Problem Statement

West Nile virus is most commonly spread to humans through infected mosquitos. Around 20% of people who become infected with the virus develop symptoms ranging from a persistent fever, to serious neurological illnesses that can result in death.

In 2002, the first human cases of West Nile virus were reported in Chicago. By 2004 the City of Chicago and the Chicago Department of Public Health (CDPH) had established a comprehensive surveillance and control program that is still in effect today.

Every week from late spring through the fall, mosquitos in traps across the city are tested for the virus. The results of these tests influence when and where the city will spray airborne pesticides to control adult mosquito populations.

As part of the Chicago's Ministry of Health department, our group has been **tasked with predicting when and where different species of mosquitos will test positive for West Nile virus.** A more accurate method of predicting outbreaks of West Nile virus in mosquitos will help the City of Chicago and CPHD more efficiently and effectively allocate resources towards preventing transmission of this potentially deadly virus. 

---

## Executive Summary

### Contents:

- [Results](#Results)
- [Business Recommendations](#Business-Recommendations)
- [Assumptions](#Assumptions)
- [Sources](#Sources)

---

### Results:

Using Random Forest Classifier, we were able to achieve a cross-validated ROC AUC score 0.85, which is considered decent. Based on the ROC curve, with a True Positive Rate of 80%, our False Positive Rate would be around 23%. This means that when we correctly predict 80% of the West Nile Virus-positive cases, we will incorrectly predict 23% of the West Nile Virus-negative cases to be positive.

---

### Business Recommendations:

We would recommend Random Forest Classifier for the purpose of our business problem. If the City of Chicago and CPHD were to use a predictive model such as the one which we have, they will be able to get a better prediction of when and where different species of mosquitos will test positive for West Nile virus so that they are able to better allocate resources and have a better idea of which mosquito to send for test.

As spraying of insectide is potentially harmful and expensive, and having to send mosquito specimens for lab test also costs money, being equipped with better information on which mosquito specimen to send for test to check if the West Nile Virus is present would lead to average yearly savings. Assuming that each lab test costs $100, these savings can be seen in the diagram above, being plotted against the True Positive Rate.

As observed in the diagram, once the True Positive Rate hits 95%, the savings then starts to drops dramatically. It is therefore recommended for the City of Chicago and CPHD to aim for a True Positive Rate of 95% in order to optimize the cost-benefits. Based on a 95% True Positive Rate, this means that as long as a specimen has a 3.3% chance or more of having the West Nile Virus, it should be sent for a lab test.

---

### Assumptions:

The results of this study and model relies on certain assumptions, one being that the distribution of West Nile Virus across the city of Chicago will not change dramatically, such that the likelihood of West Nile Virus being present in one area that it hasn't been before. With factors such as global warming, rising temperatures might cause a change in the distribution seen in the study as the years go by. Furthermore, if the cost to test whether a mosquito specimen has West Nile Virus changes greatly, the savings will change along with it.

---

### Sources:
- [Kaggle website](https://www.kaggle.com/c/predict-west-nile-virus/)
