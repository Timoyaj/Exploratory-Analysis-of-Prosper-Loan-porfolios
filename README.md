# Part I - ProsperLoan Dataset Exploration and Analysis
## By: Yaji Timothy T.


## Dataset

The dataset used is [Loan Data from Prosper](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1581581520570000): This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others. See this [data dictionary](https://www.google.com/url?q=https://docs.google.com/spreadsheet/ccc?key%3D0AllIqIyvWZdadDd5NTlqZ1pBMHlsUjdrOTZHaVBuSlE%26usp%3Dsharing&sa=D&ust=1554486256024000) to understand the dataset's variables.

In this project we focused on investigating the determining factors of loan delinquency. we created DelinquentStatus from LoanStatus. To simplify the problem of selecting delinquent loans, and to retain data, we classify all "past Due", chargedoff", cancellation,  and "defaulted" and "CurrentLoan" as delinquent, reason can be found [here](https://www.lawinsider.com/dictionary/current-loan#:~:text=Current%20Loan%20means%20an%20Eligible,such%20on%20the%20Loan%20Schedule) and all others ( "completed" and "CurrentPaymentInprogress') as None Delinquent. And encode those binary outcomes as 1 and 0, respectively. I also recode CreditScore and changed it to a categorical variable to better interprete the data. 

Most of my cleaning efforts where on handling missing values,removing duplicates, and ordering factors levels to make more intuitive sense in visualization. 

## Summary of Findings

>*  Delinquent loans constitute 15.16% of the loans in the portfolio
>* Only 7.62% of borrowers don't have their income verified have thier loans delinquent
>* Borrowers with good credit score have the highest number of delinquent loans.
>* The higest total amount of loans delinquent was from 36 months term loans which has thier purpose specified as Not available
>* Over the years delinquency fluctuates with its peaks in 2009
> * Loan monthly payment correlates with BorrowerAPR and Loan Origination Amount.
>* There is a negative relationship between  between Borrower APR with Monthly loan payment and loan original amount for loans that are delinquent. Also a positive relationship exist between loan original maount with monthly loan payment and debt to income ratio for loans that are delinquent in propser loan porfolio.
> * We observe that a positive relationship between credit score, Monthly loan payment and delinquent status. 


## Key Insights for Presentation

>* 16.80% of the loans are delinquent in the prosper Loan porfolio
>* The higest total amount of loans delinquent was from 36 months term loans which has thier purpose specified as Not available.
>* The highest number of delinquent loans are from people with good credit score rating.
>* About 54.5 percent of borrowers with delinquent loans are home owners
>* Loan delinquency fluctuates over the years with the lowest delinquent loan payment amount occuring in the year 2009.
>* There is a negative relationship between  between Borrower APR with Monthly loan payment and loan original amount for loans that are delinquent. Also a positive relationship exist between loan original maount with monthly loan payment and debt to income ratio for loans that are delinquent in propser loan porfolio.

> What is the proportion of delinquent loan in prosper porfolio?*
> What term of the loans has the higest total amount of monthly loan payment deliquent  and for what purpose was the loans taken**
> What is the Credit Score of Borrowers with the highest frequency of Loan Delinquency?**
> What is the proportion borrowers with delinquent loans that are home owners?**
> Which year has the lowest number of delinquent loans**
> Does any Relationship exit between BorrowerAPR,MonthlyLoanPayment, LoanOriginalAmount, DebtToIncomeRatio for delinquent loans?**