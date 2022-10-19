# Prosper Loan Data Exploration
## by Christina Elele


## Dataset

The dataset consisted of borrower APRs and attributes of 113,937 loans. The features included original loan amount, borrower's Prosper rating, loan term, borrower's stated monthly income, as well as many other features such as borrower's employment status, debt to income ratio, loan status etc. The dataset can be found [here] (https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv), with feature documentation available [on this page] (https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0).


## Relevant Software(s)

For this project, we explored our dataset using Jupyter Notebook after installing Anaconda. In our notebook, we imported several packages such as: Numpy, Pandas, Seaborn, Matplotlib, and Warnings, which we used to load, clean, analyse and visualise our data. 


## Summary of Findings


* We explored the borrower APR, original loan amount, income range, loan status, debt to income ratios, credit ratings, estimated returns and actual returns variables of the dataset to determine the effect they have on loan performance.

* We combined the Credit Grades variable with Prosper Rating since they both referred to the same thing and there were too many missing values in each. We also combined "Not Employed" and "Not Displayed" with $\0 for the same reason. Another tidying we did was to combine the "High Risk (HR)" and "No Credit (NC)" categories.

* One would expect that borrowers in the lower income range would take mor loans than others but from our exploration, we found that borrowers within the USD 25-000-49,999, USD 50,000-74,999 and $100,000+ income ranges took more loans than any other income group. Additionally, after we simplified our actual returns variable and explored it, we found that there was a large variation between the different loan statuses.

* Our numerical features of interest showed that there was no relationship between any of the variables. This was surprising as I had expected to see a correlation between debt to income ratios, estimated returns, and actual returns.

* Our exploration showed that median estimated returns decreased as the borrowers income range increased. This makes sense as borrowers who have higher incomes would be able to get the most competetive rates from investors. The trend between lower estimated returns and higher credit ratings was much more apparent with narrowing quartiles and lower medians. We also observed that borrowers with incomes of greater than $\75,000 may still be considered "High Risk" borrowers.

* For the different loan statuses, we found that:
    - Defaulted Loans: From the plots above, there's no relationship between estimated returns and the calculated actual return of the loans.

    - Chargedoff loans: There's also no relationship between estimated returns and actual returns for this set of loans across all credit ratings and income ranges.

    - Current Loans: We can see a slightly linear relationship between the estimated returns and actual returns. This means that if the estimated return on a loan increases, there's a small chance that the actual return on the loan will also increase and vice versa.

     - Completed Loans: For this set of loans, we can see that there is an obvious linear relationship between estimated returns and actual returns. What this means is that regardless of the return that was estimated for a particular loan, there's a possibility that the loan will always be fully paid. The reason for this might be because some borrowers repay their loans early before the due date of the loans. Hence, reducing the amount of interest they pay on their loans.

* We saw that a borrower can access higher loan amounts if their prosper rating increases. This means that there's a positive relationship between loan amount and Prosper rating — the higher the prosper rating, the higher the loan amount. This is not the same for borrower APR and Prosper rating as the borrower APR decreases with increase in prosper rating. Hence, there's a negative relationship between borrower APR and Prosper rating.

* Surprisingly, there's a slightly positive relationship between borrower APR and loan amount when the Prosper ratings increased from E to AA. This may be because people with higher ratings tend to borrow more money. If APR is increased for this set of borrowers, they'd be discouraged from borrowing more money. But people with lower credit ratings are suceptible to borrowing less money. If the APR for this set of people is reduced, they'd be encouraged to borrow a lot more.


## Key Insights for Presentation

For the presentation, I focused on features that could affect the borrower APR and loan performance, which are original loan amount, Prosper rating, debt to income ratio. 

I started by showing the distribution of Credit Rating, Income Range variable, and Debt to Income Ratio. Then, I showed the relationship between Borrower's Income, Credit Rating, and Estimated Return as well as Income, credit rating on Actual returns. I also investigated the effect of Credit rating on ralationship between income and estimated return, as well as the effect of Actual and Estimated returns on Credit Rating and Loan Staus.