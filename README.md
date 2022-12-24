# Home-Credit-Default-Risk
Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders.<br>

**Home Credit** strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. In order to make sure this underserved population has a positive loan experience, Home Credit makes use of a variety of alternative data including telco and transactional information to predict their clients' repayment abilities.

## Looking at the Big Picture

There are 7 different sources of data:

- **application_train/application_test**: The main training and testing data with information about each loan application at Home Credit. <br>Every loan has its own row and is identified by the feature SK_ID_CURR.<br> The training application data comes with the TARGET indicating ( **0**: the loan was repaid or **1**: the loan was not repaid).<br>
- **bureau**: Data concerning client's previous credits from other financial institutions.<br> Each previous credit has its own row in bureau, but one loan in the application data can have multiple previous credits.<br>
- **bureau_balance**: Monthly data about the previous credits in bureau. <br>Each row is one month of a previous credit, and a single previous credit can have multiple rows, one for each month of the credit length.
- **previous_application**: Previous applications for loans at Home Credit of clients who have loans in the application data. Each current loan in the application data can have multiple previous loans. Each previous application has one row and is identified by the feature SK_ID_PREV.
- **POS_CASH_BALANCE**: Monthly data about previous point of sale or cash loans clients have had with Home Credit. <br>Each row is one month of a previous point of sale or cash loan, and a single previous loan can have many rows.
- **credit_card_balance**: Monthly data about previous credit cards clients have had with Home Credit. <br>Each row is one month of a credit card balance, and a single credit card can have many rows.
- **installments_payment**: Payment history for previous loans at Home Credit. There is one row for every made payment and one row for every missed payment.<br>



## Our Aim:
Our objective is to predict how capable each applicant is of repaying a loan.

## The Objective in Business terms.
Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. In order to make sure this underserved population has a positive loan experience so we need to Predict whether or not a client will repay a loan or have difficulty in repaying.

## Frame of the problem
It is clearly a typical **supervised learning task** since we are given labeled training examples (each instance comes with the expected output).<br>
Moreover, it is also a typical **Classification task**, since we are asked to predict a class.<br>
It is also a univariate classification problem since we are only trying to predict a single class for each district.


## Selecting Preformance Measure
A typical performance measure for classification problems is the Area under the ROC Curve (AUC/ROC). <br> 
It is a graph showing the performance of a classification model at all classification thresholds. This curve plots two parameters:
- True Positive Rate
- False Positive Rate
