# Error-Check-Automation-

## Problem Statement

Quantitative and qualitative commentaries are reported to senior management and high level consolidated comments are provided within financial disclosures. Business controllers rely on analytics to perform sanity check and understand moves, such as fair value leveling, balance sheet geography and associate changes with market conditions. Currently, fair value leveling and seasonal inventory system commentary is conducted by manual process. Check and cross-reference between database requires large amount of repetitive work. 

## Business Requirements

An automated error check tool would be helpful to perform an assessment of appropriateness of fair value leveling and outline the addition of new accounts, unusual activity. Tool should provide high level analysis outlining the change in inventory, correlate with market data prices, inception and expiration of inventory per GL (general ledger) account and fair value level 

## Dataset

The mock-up data has 3 datatable sheets.  
![Database E-R diagram](https://github.com/mail2sabs03/Error-Check-Automation-/blob/master/Result/databaseE-R.png)

The Frogs Data is the mock-up data that we build our model upon. The raw data sheet and Vega sheet is for referencing the frogs data with related attributes to help the Fair Value Leveling. 

## Solution
* Remove duplicates, remove NAs, converting Datetime format
* Join Raw Data and Vega, compare Maturity date with Cut-off date,   determine primary Fair Value level
* Join merged table and Frogs Data, one-hot encoding predictor variables, build predicting model for remaining Fair Value Level
Model we use: Scikit-learn Decision Tree model

## Tools
We use Python to do data cleaning, model training and save the output file.


