# Use Case 1: Reducing Customer Acquisition Costs via Intelligent Data Mining (Aritificial Intelligence)

<h2>Introduction</h2>
The case is to showcase how companies can reduce their customer acquisition costs through smart data mining by leverage machine learning algorithum. We used a publicly available dataset (Note: Client's data cannot be shared due to confidential nature) to demonstrate how customer acquistion costs can be reduced dramatically. 

<h2>Challenges</h2>
We used a bank telemarketing examples to demonstrate the cost reduction via smart data mining. 

Telemarketing is a common practice for bank to promote their products or investment portfolios. Usually, it's conducted through their call centre - staff in call centre reach out to its customers by telephone, cell phone or telegram. For a typical retail bank, its customer base is huge. Hence, costs on human resources and telecommunication will influence its profitability on new product lunch. 

So, the challenges that bank faces is to find a way to locate its potential target customers in a quick and cheap way. the Question is whether we can find a smart way to dive into its customer profiles and related datasets (e.g. social and economic parameters) to predict whether a customer is likely to be a buyer for its new product. 

<h2>Data Source</h2>
UCI (https://archive.ics.uci.edu/ml/index.php) is a machine learning repository which hosts many datasets ranging from business, medical and various displines. The dataset we used to demonstrate here is a bank marketing under business category. 

<h2>Data Structure</h2>
bank client data:
1 - age (numeric) 2 - job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown') 3 - marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed) 4 - education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown') 5 - default: has credit in default? (categorical: 'no','yes','unknown') 6 - housing: has housing loan? (categorical: 'no','yes','unknown') 7 - loan: has personal loan? (categorical: 'no','yes','unknown')

related with the last contact of the current campaign:
8 - contact: contact communication type (categorical: 'cellular','telephone') 9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec') 10 - day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri') 11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.

other attributes:
12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact) 13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted) 14 - previous: number of contacts performed before this campaign and for this client (numeric) 15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')

social and economic context attributes
16 - emp.var.rate: employment variation rate - quarterly indicator (numeric) 17 - cons.price.idx: consumer price index - monthly indicator (numeric) 18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric) 19 - euribor3m: euribor 3 month rate - daily indicator (numeric) 20 - nr.employed: number of employees - quarterly indicator (numeric)

Output variable (desired target): 21 - y - has the client subscribed a term deposit? (binary: 'yes','no')

<h2>Solution Description</h2>
This is a typical classification problem in supervised machine learning. Our goal is to train the classification algorithum with historical data and screen out the non-potential customers. 

In this example, we will show case what classification algorithum can be used and what outputs each algorithum will deliver. 

The detailed code with commentory is in Customer_Acquisition.ipynb file. It can be viewed by simply click the file via github link. 

The code can also be tested locally if you've got jupyter notebook and python environment installed on your PC. 
