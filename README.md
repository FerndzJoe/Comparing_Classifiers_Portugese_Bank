# Portugese Bank : Direct Marketing Campaign 
### Determine parameters that can help future campaign to attract client to subscribe to a term deposit 
**Assignment:** Compare the performance of the classifiers (k-nearest neighbors, logistic regression, decision trees, and support vector machines) and share observations & recommendations

Dataset is from UCI Dataset: Link: https://archive.ics.uci.edu/dataset/222/bank+marketing

<img width="948" alt="image" src="https://github.com/user-attachments/assets/56564531-c135-47e2-a418-2f333bc465bf">

## Overview:
This is a practical application assignment as part of the UC Berkeley Haas AI-ML Course. The goal is to compare the performance of the classifiers (k-nearest neighbors, logistic regression, decision trees, and support vector machines). The dataset is related to the marketing of bank products over the telephone and avaialble on the UCI Website

## Business Understanding:

Comparing_Classifiers_Portugese_Bank/CRISP-DM-BANK.pdf
According to the article (link above), there were **17 campaigns** between **May 2008 and Nov 2010**. These phone campaings focused on offered **long-term deposits** with good interest rates. The **success** was determined if the **customer subscribed** to the long-term deposits.

**The focus for the bank is to identify key attributes that can help improve their success rate and attract customers to subscribe to long-term deposits.**

## Understanding the Data

The dataset comes with 21 attributes. There are no null values so all rows have information that can be utilized for data analysis and model evaluation.
There are 41188 records for us to analyze. Few of the attributes are numeric while the others are categorical.

The dataset is broken into 4 sections:

#### Bank Client data
- Age
- Job : type of job
- marital : marital status
- education
- default: has credit in default?
- housing: has housing loan?
- loan: has personal loan?

#### Information related with the last contact of the current campaign
- contact: contact communication type
- month: last contact month of year
- day_of_week: last contact day of the week
- duration: last contact duration, in seconds

#### Other Attributes
- campaign: number of contacts performed during this campaign and for this client
- pdays: number of days that passed by after the client was last contacted from a previous campaign
- previous: number of contacts performed before this campaign and for this client
- poutcome: outcome of the previous marketing campaign

#### Social and Economic context attributes
- emp.var.rate: employment variation rate - quarterly indicator (numeric)
- cons.price.idx: consumer price index - monthly indicator (numeric)
- cons.conf.idx: consumer confidence index - monthly indicator (numeric)
- euribor3m: euribor 3 month rate - daily indicator (numeric)
- nr.employed: number of employees - quarterly indicator

#### Target Variable
- y - has the client subscribed a term deposit? (yes or no)

#### Missing Data needing special attention
- There are a few records that has a value of 'unknown' and it represents missing data. The attributes with these missing values are: `job`, `education`, `default`, `housing`, and `loan`.
- The attribute `pdays` has a value of 999 indicating that the client was not previously contacted
- The attribute `duration` highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.



