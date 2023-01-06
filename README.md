# Credit Card Fraud Prediction

<img src="https://i.imgur.com/pWBEwXX.png" />

<h2>Problem statement</h2>
While the current fraud rate at a large financial institution is about 5%, the company has been experiencing an upward trend in credit card fraud. From the available dataset, the fraud rate has increased from 1% in 2020 to 4% in 2021. This trend not only increases the risk of reputational damage but also the possibility of customers losing trust in the company. The situation is bad that it may cause the company to lose existing customers and hamper its ability to attract new customers. The company needs to take drastic actions now to reverse the trend.

<br></br>
In this project, I attempt to use machine learning to help a large financial institution actively flag fraud at the 5% false positive rate.

<h2>Languages and Libraries Used</h2>

- R programming language 
- [List of libraries](https://github.com/graphshade/credit_card_fraud/blob/main/renv.lock)

<h2>Environment Used </h2>

- <b>Ubuntu 22.04.1 LTS</b>


<h2>Key Insight:</h2>

Operating at the 5% false positive rate means that the company is willing to accept the model wrongly flagging 5 out of every 100 transactions as fraudulent. While this decreases the model's precision rate, it boosts the model's recall rate. 

At 5% false positive rate, we found at that we have to flag a transaction as fraud if the predicted probability is equal to or greater than 33%. At this threshold, we estimate the model’s recall rate at 85% which means that 85% of the time, the model is capable of correctly predicting actual fraud cases. 

<h2>Recommendations:</h2>

1. The financial instutition should introduce a second layer of transaction approval for transactions with adjustment value below $50. An observation with transaction adjustment value represent a transaction involving a second currency other than USD. From the analysis, it is known that the rate of fraud among credit card transactions with transaction adjustment value below $50 is about 34%. We also know that fraud prevalence is low when the transaction adjustment value is high.
In effect, introducing this second layer of transaction approval (which may be an OTP sent via mail or SMS for transaction approval) in targeted regions with low transaction adjustment value will serve as a gatekeeper against credit card fraud.

2. Targeted education of credit card holders with older account age will equally go to reduce credit card fraud. Credit card fraud is continuously evolving such that there is a need to constantly keep customers aware of recent tactics in credit card fraud so that they are actively on the lookout for such gimmicks. 


<h2>Reproducing the Analysis:</h2>

<p align="left">

1. [Install R and RStudio](https://techvidvan.com/tutorials/install-r/)
 
2. Clone the project: Run this from the command line
 
 ```commandline
 git clone https://github.com/graphshade/loan_default.git
 ```
 
3. Install Required Libraries Using Virtual Environment: 
   
   You may install the libraries directly on your computer however, using the virtual environment library `renv`. [Follow this guide to install renv](https://www.youtube.com/watch?v=yc7ZB4F_dc0)
   1. Open the app.R file in RStudio
   2. In the RStudio console run `renv::init()` to initiate the renv virtual environment and install the required libraries from the [renv.lock](https://github.com/graphshade/loan_default/blob/main/renv.lock) file 
