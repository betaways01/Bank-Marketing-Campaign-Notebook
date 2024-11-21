# Bank Marketing DataSet - Intelligent Targeting:
***
## Marketing Introduction:
*The process by which companies create value for customers and build strong customer relationships in order to capture value from customers in return.*

**Kotler and Armstrong (2010).**
***

**Marketing campaigns** are characterized by  focusing on the customer needs and their overall satisfaction. Nevertheless, there are different variables that determine whether a marketing campaign will be successful or not. There are certain variables that we need to take into consideration when making a marketing campaign. <br>

## The 4 Ps:
1) Segment of the <b>Population:</b> To which segment of the population is the marketing campaign going to address and why? This aspect of the marketing campaign is extremely important since it will tell to which part of the population should most likely receive the message of the marketing campaign. <br><br>
2) Distribution channel to reach the customer's <b>place</b>: Implementing the most effective strategy in order to get the most out of this marketing campaign. What segment of the population should we address? Which instrument should we use to get our message out? (Ex: Telephones, Radio, TV, Social Media Etc.)<br><br>
3) <b> Price:</b> What is the best price to offer to potential clients? (In the case of the bank's marketing campaign this is not necessary since the main interest for the bank is for potential clients to open depost accounts in order to make the operative activities of the bank to keep on running.)<br><br>
4) <b> Promotional</b> Strategy: This is the way the strategy  is going to be implemented and how are potential clients going to be address. This should be the last part of the marketing campaign analysis since there has to be an indepth analysis of previous campaigns (If possible) in order to learn from previous mistakes and to determine how to make the marketing campaign much more effective.

# Outline: <br>
***
A. **Attribute Descriptions**<br>
I. *[Bank client data](#bank_client_data)<br>
II. *[Related with the last contact of the current campaign](#last_contact)<br>
III. [Other attributes](#other_attributes) <br>

B. **Structuring the data:** <br>
I. *[Overall Analysis of the Data](#overall_analysis)<br>
II. *[Data Structuring and Conversions](#data_structuring) <br>

C. **Exploratory Data Analysis (EDA)**<br>
I. *[Accepted vs Rejected Term Deposits](#accepted_rejected) <br>
II. *[Distribution Plots](#distribution_plots) <br>

D. **Different Aspects of the Analysis: **<br>
I. *[Months of Marketing Activty](#months_activity) <br>
II. *[Seasonalities](#seasonality) <br>
III. *[Number of Calls to the potential client](#number_calls) <br>
IV. *[Age of the Potential Clients](#age_clients) <br>
V. [Types of Occupations that leads to more term deposits suscriptions](#occupations) <br>

E. **Correlations that impacted the decision of Potential Clients.**
I. *[Analysis of our Correlation Matrix](#analysis_correlation) <br>
II. *[Balance Categories vs Housing Loans](#balance_housing)<br>
III. [Negative Relationship between H.Loans and Term Deposits](#negative_relationship) <br>

F. ** Classification Model **<br>
I. [Introduction](#classification_model)<br> 
II. [Stratified Sampling](#stratified)<br>
III. [Classification Models](#models)<br>
IV. [Confusion Matrix](#confusion)<br>
V. [Precision and Recall Curve](#precision_recall)<br>
VI. [Feature Importances Decision Tree C.](#decision) <br>

G. ** Next Campaign Strategy**<br>
I. [Actions the Bank should Consider](#bank_actions)<br>

# A. Attributes Description: <br>

Input variables:<br>
# Ai. bank client data:<br>
<a id="bank_client_data"></a>
1 - **age:** (numeric)<br>
2 - **job:** type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')<br>
3 - **marital:** marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)<br>
4 - **education:** (categorical: primary, secondary, tertiary and unknown)<br>
5 - **default:** has credit in default? (categorical: 'no','yes','unknown')<br>
6 - **housing:** has housing loan? (categorical: 'no','yes','unknown')<br>
7 - **loan:** has personal loan? (categorical: 'no','yes','unknown')<br>
8 - **balance:** Balance of the individual.
# Aii. Related with the last contact of the current campaign:
<a id="last_contact"></a>
8 - **contact:** contact communication type (categorical: 'cellular','telephone') <br>
9 - **month:** last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')<br>
10 - **day:** last contact day of the week (categorical: 'mon','tue','wed','thu','fri')<br>
11 - **duration:** last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.<br>
# Aiii. other attributes:<br>
<a id="other_attributes"></a>
12 - **campaign:** number of contacts performed during this campaign and for this client (numeric, includes last contact)<br>
13 - **pdays:** number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)<br>
14 - **previous:** number of contacts performed before this campaign and for this client (numeric)<br>
15 - **poutcome:** outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')<br>

Output variable (desired target):<br>
21 - **y** - has the client subscribed a term deposit? (binary: 'yes','no')

