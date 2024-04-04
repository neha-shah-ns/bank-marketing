# Customer Classification and Prescriptive Modeling of Portuguese Bank Marketing

## PROBLEM  

Market segmentation is a critical component of any modern marketing mix and plays a major role in bank marketing. By identifying and defining discrete marketing segments of a target market, bank marketers can specialize their approaches to messaging, channel selection, seasonality, and other factors based on the preferences and attitudes associated with the demographic identifiers attached to each segment. With the advent of large marketing databases, the challenge of revenue projection has fallen on the shoulders of marketers more frequently. Using modern modeling techniques, marketers can produce prescriptive closing rates for consumers at various stages of the sales pipeline, providing financial executives with a powerful tool to use in projecting earnings. 

Our aim is to answer the following question: Can effective marketing segments be derived from observing the attributes of respondents to previous marketing campaigns? 
Additionally, we want to research if attributes of previous buyers can predict closing probability as well as if seasonality has an effect on closing. To answer these questions, we will explore Portuguese bank-full dataset which can be found here. https://archive.ics.uci.edu/dataset/222/bank+marketing

## DATA 

The data was collected from a Portuguese bank that used its personal contact-center to do directed marketing campaigns, targeting a specific set of contacts. The goal of the multiyear campaign was to procure new term deposits which is defined as locking money up for a specific period of time to secure higher interest payments. Within a campaign, an agent makes phone calls to a list of clients to sell the deposit (outbound) or, if the client calls the contact-center for any other reason, they are asked to subscribe the deposit (inbound). Thus, the result is a binary unsuccessful or successful contact.
The data collected was from May 2008 to November 2010 and includes 16 attributes as shown

![image](https://github.gatech.edu/storage/user/58706/files/06727882-b720-4b4a-9924-17ac9de582e8)

## APPROACH/METHODOLOGY 

I. Exploratory Data Analysis / Data Preparation

* Conduct univariate and multivariate analysis to identify attributes that may require transformation or removal and find large-scale patterns that could could provide basis to model selection or data subsetting

* Engineer a time series variable to allow for analysis of seasonality/trends

* Convert factorial attributes to dummy variables, create training and testing datasets, subset data between campaign-focused data and demographic-data

II. Segmentation/Customer Profiling

* Utilize a PAM Clustering model to build potential profiles for target markets

* Utilize a Random Forest model to extract highly influential demographic attributes

III. Prescriptive Modelling

* Find a reliable classification model from which to predict binary closing outcomes, utilizing support vector machines (SVM) and k-means techniques

* Explore several variable selection techniques to find the best possible logistic regression model to calculate closing probabilities to use in lead scoring and revenue projection

## RESULTS 

![image](https://github.com/nshah-11/bank-marketing/assets/97864887/c0f408cc-7b51-4342-aa71-fbcb29cb479c)

![image](https://github.com/nshah-11/bank-marketing/assets/97864887/8c4e30f9-596a-47be-9822-00f3e89c006f)

![image](https://github.com/nshah-11/bank-marketing/assets/97864887/80182328-9b92-4be2-bb32-40f62c9668c3)

![image](https://github.com/nshah-11/bank-marketing/assets/97864887/3b7482aa-868a-4fd2-aa4e-34b8d6107f7a)

![image](https://github.com/nshah-11/bank-marketing/assets/97864887/a9672036-352c-4fd1-b74a-6250c6193b47)

![image](https://github.com/nshah-11/bank-marketing/assets/97864887/d6548ca7-092a-4af1-b34d-8745d0388df1)

## RECOMMENDATIONS 

Based on our EDA and the results of the models above, we have settled on the following list of recommendations for the bank in our study:

* Widen the scope of data collection for future – low explainability scores across the board suggest that there could be much to gain from enriching the database with further attributes.

* Consider more advanced methods for dealing with missing values and outliers, either through imputation or the development of a nuanced set of standards for removing observations with problematic data.

* Based on the PAM Clustering model, a representative customer profile for successfully converted leads is as follows: average age between 36 and 44, married, holds a secondary or tertiary education, and have a job type of technician, blue collar, or management. The bank should dedicate a portion of its marketing mix to generating leads that fit these descriptors. Measuring variable importance with Random Forest supported emphasis on job and a similar age group.

* Dedicate a portion of the marketing mix to collecting leads on the extreme ends of the employment spectrum – our Logistic Regression models suggested that whether each lead was either a student or a retiree had the greatest positive impact on closing probability, this could be the basis of a secondary target market

* Consider ways to target or optimize scripts for individuals with relatively low bank account balances, as those individuals appeared to convert to term loans at a higher rate. Conversely, the bank should consider avoid collecting leads that carry personal or housing loans or develop new materials to overcome objections from said leads, as our Logistic Regression models suggested that each was a leading factor in reducing closing probability.

* Use Logistic Model #3 as a basis for revenue projection from current lead pipeline – By attaching, to each record, a median number for expected lifetime revenue from a successful close, the firm could multiply the revenue by the logit output from the model to produce an estimate for the value of each lead, and our performance metrics suggest it would at least moderately better than a simple average of overall past closing probability.
 
## NAVIGATING THROUGH THIS PROJECT 
Here is an outline of what materials you can for this project and where.

* CODE: All coding was done in R. This includes an rmd file for EDA as well as R files each model that was built. These files can be run using RStudio.  

* DATA: In addition to the UCI website, the bank_full dataset we analyzed can be found here to download. 
  
Contributors: Neha Shah, Michael Holley, Suganya Natarajan, Divya Chandrasekaran
