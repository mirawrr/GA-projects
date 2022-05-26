
# Project 3: Subreddit Classifier - Tea or Coffee?


This project aims to develop the best classification model that can accurately distinguish textual data on coffee and tea. 
We tap on posts in subreddits r/coffee and r/tea to form the corpus o our modelling process. 

We tested several combinations of transformer and estimator models including CountVectorizer, 
Term Frequency-Inverse Document Frequency Vectorizer, Logistic Regression, Multinomial Naive Bayes and Random Forest. 

## Problem Statement

We are a team of data scientists working for Coffea Vibes, a beverage company. 
The company is venturing into e-commerce and will be launching its own website/application selling coffee and tea products to consumers. 

We have been tasked to build a classification model that can accurately distinguish between coffee and tea in textual data.

Our classification model will contribute to the following use cases: 
* Our web development team can optimise the recommender systems so as to accurately suggest related products and advertisements to our potential consumers who might have varying preferences for coffee or tea.
* Our business insights team can leverage on the classification model to correctly distinguish customer feedback on coffee and tea (e.g. through emails) and comments made on the company's social media pages, to aid better understanding of customer's feedback and take appropriate actions quickly, if necessary. 

We evaluated the models based on the following criteria:
* Accuracy scores (the higher, the better)
* Delta between train and test scores (the smaller, the better)
* Clear distinction of important features i.e. words to distinguish coffee and tea

## Data Dictionary

When we acquired the reddit datasets through API, we retrieved numerous data with over 80 features. However, not all columns were 
useful for our analysis. 

These are the features that we focused on: 

|Feature|Type|Description|
|---|---|---|
|created_utc|*string*|Time of post created|
|removed_by_category|*string*|Status of post used for filtered out removed or deleted posts|
|title|*string*|Title of post (mandatory field)|
|selftext|*string*|Body text of post (optional field)|
|clean_full_text|*string*|Title and body text merged into one column and cleaned|
|num_chars|*int*|No. of characters in clean_full_text|
|num_words|*int*|No. of words in clean_full_text|




## Structure

This project is organised into three notebooks: 

- Notebook 1 : Data Acquisition
- Notebook 2: Data Cleaning & Exploratory Data Analysis 
- Notebook 3: Modelling & Model Evaluation

## Summary of Analysis

The Multinomial Naive Bayes with CountVectorizer model was the best performing model, produced an accuracy score of 0.88. 

The comparison of model scores are as follows: 

| Method | Train Score | Test Score (Accuracy) |Delta|Evaluation|
| :-: | :-: | :-: | :-:|:-:|
| Baseline | - | 0.52 | -|-|
| CountVect + Multi NB | 0.93 | 0.88| 0.05 | 1st |
| TF-IDF + Log Regression | 0.96 | 0.87 | 0.09 |2nd |
|TF-IDF + Multi NB | 0.95 | 0.86 | 0.09 | 3rd |
| CountVect + Log Regression | 0.99 | 0.85 | 0.14 |4th |
| CountVect + Random Forest | 1.0 | 0.84 | 0.16 |5th |
| TF-IDF + Random Forest | 1.0 | 0.83 | 0.17 | 6th |





   

## Conclusions & Recommendations

Our company can utilise the following distinguishing keywords in their respective use cases e.g. to optimise the recommenders system or to generate business insights: 

| Top Keywords in Tea Class | Top Keywords in Coffee Class|
| :-: | :-: |
|oolong|machine|
|puerh|grinder|
|sencha|grind|
|jasmine|burr|
|china|espresso|
|matcha|aeropress|
|herbal|bean|
|teapot|moka|
|earl|roaster|
|grey|ground

For instance, if a customer search for 'oolong' on our website, we can infer that he would be interested in tea-related products, and so recommend tea-related products to him/her and direct related advertisement as well. The same goes for coffee-related keywords. 

This classification model is binary, and is an initial step in building up our company's capabilities. We can build on this foundation and develop a multi-class classification that can accurately distinguish different beverages sold by our company as well. 
## Limitations & Next Steps

* The reddit posts seem to be highly skewed to the US market. For future iterations, to consider data collection from alternative sources esp. regional or local forum pages. 
* This project focused only on textual data, but the reddit posts show that consumers are relying on other methods of communication such as using external links, images and videos which in itself might contain unique insights. We can explore studying other visual methods of communication in the future.  
* We extracted a lot more reddit data than what was explored in this project. Further iterations might consider looking closer into other datapoints such as the number of comments (indication of the traction received on a particular item/topic) and also the 'tags' attached to each post. 

**Possible Improvements**
* To test the selected model on truly unseen data i.e. freshly scraped from reddit again. 
* To explore other hyperparameter tuning methods to improve the best score and test score. 
* To identify noise in the data based on the important features revealed by the models, repeat data cleaning steps to eliminate noise and re-run the models again. 