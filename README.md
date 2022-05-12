# Signifyd-Challenge
This repository contains the project code used for the Signifyd challenge for the role of Data Science intern

## Introduction
One useful data point in detecting fraud is the account history of a customer.
For an account, we receive notification of purchases and, sometimes, reports of fraud.
Typically, a prior report of fraud for an account would increase the perceived risk of fraud on future
transactions.
Similarly, a history of non-fraudulent purchases for an account would decrease the risk of fraud. A
credit card holder has 90 days to report any fraudulent transactions with the card. So if an account
has purchases over 90 days old and no reports of fraud, we assume that these older purchases
were not-fraudulent.

## Problem Statement
The purpose of this programming problem is to determine the status of a customer account history at
the time a new purchase is made.
The input is a sequence of customer account events, in chronological order. Each event has three
fields, all of which are of string type
<DATE>,<CUSTOMER_ACCOUNT_ID>,<EVENT_TYPE>

 ## For example:
2015-01-01,joe@signifyd.com,PURCHASE
  
2015-02-01,fraudster@fraud.com,FRAUD_REPORT
There are two event types:
1. PURCHASE - indicates a purchase by this customer account on the specified date.
2. FRAUD_REPORT - indicates we received a report of fraud associated with this customer
account. The specified date is that date that we received the report, not the date the fraud
was committed.
For each eventPURCHASE, we are interested in a summary of the customer account history based on
prior events. The summary consists of the date of the summary, the customer account id, and a
status.
There are four possible values for the status of the customer account history:
1. NO_HISTORY - there are no prior events for this customer account
2. FRAUD_HISTORY - we have at least one event FRAUD_REPORTfor this customer account.
3. GOOD_HISTORY- customer account has no FRAUD_REPORTs and at least one prior that
PURCHASEis more than 90 days old.
4. UNCONFIRMED_HISTORY - customer account has no FRAUD_REPORTs and at least one
priorPURCHASEbut no PURCHASEs over 90 days old.

For accounts with FRAUD_HISTORY, GOOD_HISTORY, and UNCONFIRMED_HISTORY, the status
also contains a count of relevant events.
● FRAUD_HISTORY - count of FRAUD_REPORTs
● GOOD_HISTORY - count of priorsPURCHASE over 90 days old
● UNCONFIRMED_HISTORY- count of prior purchases.
  
## Documentation
1. [Dataset](https://drive.google.com/file/d/1-f9p_BWf-JtM06eWxssGl20uHFvS9H6I/view?usp=sharing)
2. [Google Colab](https://github.com/SaiTulasi69/Signifyd-Challenge/blob/main/Signifyd_Challenge.ipynb)
  
## Support
Having trouble understanding or implementing this challenge? Check out the [documentation](https://github.com/SaiTulasi69/Signifyd-Challenge/edit/main/README.md#documentation) or create a pull request and I could help you sort it out.
