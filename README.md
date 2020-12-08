# Brands Sentiment Prediction with NLP

##### Authors: [ Ignacio Ruiz](https://github.com/carlosiruiz " Ignacio Ruiz"), [Ismael Araujo](https://github.com/Ismaeltrevi "Ismael Araujo")

![](https://api.time.com/wp-content/uploads/2016/02/twitter-algorithmic-filtering-missed-tweets.jpg)

Repository Structure

       `├── eda     | All the images used in the README and Presentation
        ├── images          | Images used
        ├── Main Notebook.ipynb | Walkthough the EDA and Vanilla Models       
   	    ├── README.md | This document!
   	    └── Main Notebook.ipynb | Walkthough the EDA and Vanilla Models       

### Business Problem

Nowadays, more people are using social media to express problems and compliments to companies. It is an easy and cheap way for companies to get feedback from consumers. However, the larger a company is, the more difficult it gets to analyze what people are talking about and how a company should improve. Feedback is valuable information that is difficult to get and can be expensive to collect. Thus, creating a way to automate sentiment detecting and critical points that people are talking about can help companies improve their products.

### Business Questions

1. Can a model predict companies' sentiment perception on tweets?
2. Does sentiment analysis perform better on raw tweets or cleaned tweets?

### Data

It was used around 18,000 web scrapped tweets mentioning Google and Apple using Twint. It was collected information such as the tweet text, language, location, date, and username. It was also a dataset from CrowdFlower provided by Flatiron School with 9,093 observations with the tweet text, a keyword, and the emotion. The emotion was divided in Nagative, Positive, and No emotion toward brand or product.

![](https://github.com/carlosiruiz/mod_4_nlp/blob/main/images/sentiment-analysis-1.png?raw=true)

### Methodology

#### Preprocessing

For preprocessing the data, we create different columns for each stage of the data cleaning, so we could compare how each model would perform with each stage. The stages were:

- Raw Tweets
	- We did not do any data cleaning for the raw tweets
- Cleaned Tweets
	- We did some data cleaning, such as removing numbers and punctuation
- Only English Words
	- We removed all the numbers and any word that isn't in the English dictionary

#### Models and Feature Engineering

We tested a few classification models, such as Logistic Regression using F1 Micro Score, KNN, Random Forest, and Grid Search running Random Forest. Since the *company* feature had the name of products (such as iPhone, iPad, Android, Mac etc.), we created a feature with the main company name (Apple o Google). We also made features using Lemmatization and Stemming.

![](https://github.com/carlosiruiz/mod_4_nlp/blob/main/images/word_cloud.png?raw=true)

We tested these models using different stages of data cleaning and feature engineering and analyzed how each model performed with each of the features that were engineered.

### Conclusion

Our final best performing used Logistic Regression with TDIDF vectorizer with a 0.8284 accuracy.

Using sentiment analysis can be used as a baseline prediction model.
Using sentiment analysis creates a better understanding in trends company's product response.

We recommend companies to use NLP to be able to collect and interpret what consumers are writing on social media. It's a valuable data and should take in consideration when the company takes decisions.


![](https://github.com/carlosiruiz/mod_4_nlp/blob/main/images/model_heatmap.png?raw=true)












