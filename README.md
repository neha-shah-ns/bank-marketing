# Customer Classification and Prescriptive Modeling of Portuguese Bank Marketing

## PROBLEM  

Market segmentation is a critical component of any modern marketing mix and plays a major role in bank marketing. By identifying and defining discrete marketing segments of a target market, bank marketers can specialize their approaches to messaging, channel selection, seasonality, and other factors based on the preferences and attitudes associated with the demographic identifiers attached to each segment. With the advent of large marketing databases, the challenge of revenue projection has fallen on the shoulders of marketers more frequently. Using modern modeling techniques, marketers can produce prescriptive closing rates for consumers at various stages of the sales pipeline, providing financial executives with a powerful tool to use in projecting earnings. 

![image](https://github.gatech.edu/storage/user/58706/files/5b17b480-fbec-493b-bcb3-12f4fae2bad8)

Our aim is to answer the following question: Can effective marketing segments be derived from observing the attributes of respondents to previous marketing campaigns? 
Additionally, we want to research if attributes of previous buyers can predict closing probability as well as if seasonality has an effect on closing. To answer these questions, we will explore Portuguese bank-full dataset which can be found here. https://archive.ics.uci.edu/dataset/222/bank+marketing

## DATA 

The data was collected from a Portuguese bank that used its personal contact-center to do directed marketing campaigns, targeting a specific set of contacts. The goal of the multiyear campaign was to procure new term deposits which is defined as locking money up for a specific period of time to secure higher interest payments. Within a campaign, an agent makes phone calls to a list of clients to sell the deposit (outbound) or, if the client calls the contact-center for any other reason, they are asked to subscribe the deposit (inbound). Thus, the result is a binary unsuccessful or successful contact.
The data collected was from May 2008 to November 2010 and includes 16 attributes as shown

![image](https://github.gatech.edu/storage/user/58706/files/06727882-b720-4b4a-9924-17ac9de582e8)

## APPROACH/METHODOLOGY 

I. Exploratory Data Analysis / Data Preparation

* Conduct univariate and multivariate analysis to identify potentially problematic attributes that may require transformation or removal and find large-scale patterns that could inform model-selection or data-subsetting

* Engineer a time-series variable to allow for analysis of seasonality/trends

* Convert factorial attributes to dummy variables, create training and testing datasets, subset data between campaign-focused data and demographic-data

II. Segmentation/Customer Profiling

* Utilize a PAM Clustering model to build potential profiles for target markets

* Utilize a Random Forest model to extract highly influential demographic attributes

III. Prescriptive Modelling

* Find a reliable classification model from which to predict binary closing outcomes, utilizing support vector machines (SVM) and k-means techniques

* Explore several variable selection techniques to find the best possible logistic regression model to calculate closing probabilities to use in lead scoring and revenue projection

## FINDINGS 

Based on our EDA and the results of the models above, we have settled on the following list of recommendations for the bank in our study:

* Widen the scope of data collection for future – low explainability scores across the board suggest that there could be much to gain from enriching the database with further attributes.

* Consider more advanced methods for dealing with missing values and outliers, either through imputation or the development of a nuanced set of standards for removing observations with problematic data.

* Based on the PAM Clustering model, a representative customer profile for successfully converted leads is as follows: average age between 36 and 44, married, holds a secondary or tertiary education, and have a job type of technician, blue collar, or management. The bank should dedicate a portion of its marketing mix to generating leads that fit these descriptors. Measuring variable importance with Random Forest supported emphasis on job and a similar age group.

* Dedicate a portion of the marketing mix to collecting leads on the extreme ends of the employment spectrum – our Logistic Regression models suggested that whether each lead was either a student or a retiree had the greatest positive impact on closing probability, this could be the basis of a secondary target market

* Consider ways to target or optimize scripts for individuals with relatively low bank account balances, as those individuals appeared to convert to term loans at a higher rate. Conversely, the bank should consider avoid collecting leads that carry personal or housing loans or develop new materials to overcome objections from said leads, as our Logistic Regression models suggested that each was a leading factor in reducing closing probability.

* Use Logistic Model #3 as a basis for revenue projection from current lead pipeline – By attaching, to each record, a median number for expected lifetime revenue from a successful close, the firm could multiply the revenue by the logit output from the model to produce an estimate for the value of each lead, and our performance metrics suggest it would at least moderately better than a simple average of overall past closing probability.
 
## NAVIGATING THROUGH THIS PROJECT 
Here is an outline of what materials you can for this project and where.

* CODE: This includes R files of initial EDA as well as code for each model utilized. 

* DATA: In addition to the UCI website, the bank_full dataset we analyzed can be found here to download. 

* FINAL CODE: This includes our entire code for EDA combined into one RMD file. 

* FINAL REPORT: We have written a 8-10 page report available as a PDF to download. 

* OTHER RESOURCES: N/A

* PROGRESS REPORT: Here is a draft of our final report available for download as a pdf.  

* PROJECT PROPOSAL: Here we outline the grounds for our project and what we attempt to explore.

* PROPOSAL PRESENTATION: This includes our ppt slides for our proposal presentation which can be found here. To watch the video presentation, please go to  https://www.youtube.com/watch?v=ZclsIvkVix0

* VISIUALIZATIONS: N/A
  
Contributors: Neha Shah, Michael Holley, Suganya Natarajan, Divya Chandrasekaran
