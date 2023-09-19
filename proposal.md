# Textual Analysis of Amazon Grocery and Gourmet Food Product Reviews.

-  Author : Manimadhuri Edara
-  Prepared for UMBC Data Science Master Degree Capstone by Dr Chaojie (Jay) Wang
-  GitHub profile: <a href="https://github.com/MANIMADHURIE"> MANIMADHURIE </a>
-  LinkedIn progile: <a href="https://www.linkedin.com/in/manimadhuriedara/"> manimadhuriedara </a>
-  PowerPoint Presentation - TBA
-  YouTube Video - TBA
  
## Objective

In this project I aim to employ natural language processing (NLP) techniques and sentiment analysis in conjunction with a machine learning model, utilizing both the textual content of the 'review text' and the numerical 'overall' rating columns, to classify reviews into distinct sentiment categories, namely positive, negative, or neutral. Also develop a collaborative filtering recommendation system using user-item interactions and latent factor modeling to generate personalized product ('asin') recommendations, leveraging historical review data and user preferences.

## Background
The Text Analysis of Amazon Grocery_and_Gourmet_Food Product Reviews will provide a comprehensive analysis of customer reviews and ratings for food products on the Amazon Fresh platform. By delving into this dataset, through natural language processing and machine learning techniques, seek to uncover trends and patterns that can inform businesses, consumers, and the broader food industry.

<img src="https://assets.aboutamazon.com/dims4/default/e1f08b0/2147483647/strip/true/crop/1279x720+0+0/resize/1320x743!/format/webp/quality/90/?url=https%3A%2F%2Famazon-blogs-brightspot.s3.amazonaws.com%2Ff5%2F9f%2F43fe106c4a5081e7a696ef0a8fa8%2Ffresh-1280x7201.jpg" width="400">

- What is it about?
  
  To analyze the content of the reviews and perform tasks like text classification, topic modeling, sentiment analysis and extract valuable insights into 
  consumer preferences, product quality, and reviewer behavior
  
- Why does it matter?

  Text analysis of Amazon grocery product reviews has significance since it can provide businesses, consumers, and the food industry with valuable insights by 
  identifying trends and patterns in Amazon food product reviews.
  
- What are your research questions?
 
  1. **Reviewer Behavior:**
     - Identify patterns in reviewer behavior, such as frequent reviewers or those who tend to leave extreme ratings.
  2. **Review Text Classification:**
     - Categorize reviews into specific topics or categories based on the content of the review text.
  3. **Spam Detection:**
     - Develop a method to detect duplicate reviews or spam reviews that may artificially inflate or deflate product ratings.
  4. **Comparative Analysis:**
     - Compare the sentiment and content of reviews for different products or brands within the dataset.

## Data

The Amazon Grocery_and_Gourmet_Food Reviews dataset consists of reviews of Grocery_and_Gourmet foods from Amazon. The data span a period of more than 10 years, including all ~500,000 reviews. Reviews include product and user information, ratings, and a plaintext review.
The Amazon Grocery_and_Gourmet_Food Reviews dataset is a valuable resource to understand consumer behavior and the online review process. It is a large and comprehensive dataset that can be used to answer a variety of research questions.

##### Description
- Data sources : https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/
- Data size (MB, GB, etc.) : 91.716MB
- Data shape (# of rows and # columns):
   - Rows: 151254
   - Columns: 9
- Time period : 2000 - 2014
- Data dictionary:

  ![image](https://github.com/DATA-606-2023-FALL-TUESDAY/Edara_Manimadhuri/assets/37103568/876ff8d2-907e-491f-ada5-18e7359b910d)


          
- Target/label in your ML model : overall
  
- Features of the model = ['reviewText', 'overall', 'summary', 'unixReviewTime', 'reviewTime']

## Exploratory Data Analysis (EDA)

TBA

## Model Training

TBA

## Application of the Trained Models

TBA

## Conclusion

TBA

## References
 [1] Sentiment Analysis on Amazon Product Reviews using Text Analysis and Natural Language Processing Methods, April 2023, 
 https://www.researchgate.net/publication/369997867_Sentiment_Analysis_on_Amazon_Product_Reviews_using_Text_Analysis_and_Natural_Language_Processing_Methods

 [2] Bi-RNN and Bi-LSTM Based Text Classification for Amazon Reviews, April 2023, https://www.researchgate.net/publication/370062640_Bi-RNN_and_Bi-LSTM_Based_Text_Classification_for_Amazon_Reviews

 [3] Performance Evaluation of Feature Selection Methods for Sentiment Classification in Amazon Product Reviews, July 2023, 
 https://www.researchgate.net/publication/373266249_Performance_Evaluation_of_Feature_Selection_Methods_for_Sentiment_Classification_in_Amazon_Product_Reviews
  
 [4] Justifying recommendations using distantly-labeled reviews and fined-grained aspects, 2019, https://cseweb.ucsd.edu//~jmcauley/pdfs/emnlp19a.pdf
