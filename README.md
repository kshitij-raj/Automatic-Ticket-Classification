# Automatic Ticket Classification

## Problem Statement
For a financial company, customer complaints carry a lot of importance, as they are often an indicator of the shortcomings in their products and services. If these complaints are resolved efficiently in time, they can bring down customer dissatisfaction to a minimum and retain them with stronger loyalty. This also gives them an idea of how to continuously improve their services to attract more customers. 

These customer complaints are unstructured text data; so, traditionally, companies need to allocate the task of evaluating and assigning each ticket to the relevant department to multiple support employees. This becomes tedious as the company grows and has a large customer base.

## Business Goals
Build a model that is able to classify customer complaints based on the products/services. By doing so, Model can segregate these tickets into their relevant categories and, therefore, help in the quick resolution of the issue.

Analyse patterns and classify tickets into the following five clusters based on their products/services:

 - Credit card / Prepaid card
 - Bank account services
 - Theft/Dispute reporting
 - Mortgages/loans
 - Others 

## Dataset
[Dataset link]('https://drive.google.com/file/d/1Y4Yzh1uTLIBLnJq1_QvoosFx9giiR1_K/view')

The data set given to you is in the .json format and contains 78,313 customer complaints with 22 features. You need to convert this to a dataframe in order to process the given complaints.

## Model Building Approach
-  Data loading

- Text preprocessing
    * Make Text lowercase.
    * Remove text in square bracket.
    * Remove Punctuation.
    * Remove words containg numbers.
    * Lemmatize texts.
    * Use POS tags to get relevant words from the texts.

- Exploratory data analysis (EDA)
    * Visualise the data according to the 'Complaint' character length
    * Using a word cloud to visualise the top 40 words by frequency among all the articles after processing the text
    * Found the top unigrams,bigrams and trigrams by frequency among all the complaints after processing the text. ‘

- Feature extraction
    * Convert the raw texts to a matrix of TF-IDF features

- Topic modelling using NMF
    * Perform Manual Topic Modelling.
    * Create the best topic and assign topic to complaints.

- Model building using supervised learning
    * Build Logistic Regression, Decision Tree, and Random Forest Model

- Model training and evaluation

- Model inference
    * Used best model to predict a  custom text to see its performance. 