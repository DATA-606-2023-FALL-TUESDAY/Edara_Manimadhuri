# Text Analysis of Amazon Grocery_and_Gourmet_Food Product Reviews.
### Name : Manimadhuri Edara
### GitHub profile: https://github.com/MANIMADHURIE
### LinkedIn progile: https://www.linkedin.com/in/manimadhuriedara/
### Introduction
The "Amazon Grocery and Gourmet Food Reviews" project is a comprehensive analysis of customer reviews and ratings for food products on the Amazon Fresh platform. By delving into this dataset, I aim to extract valuable insights into consumer preferences, product quality, and reviewer behavior. Through natural language processing and machine learning techniques, seek to uncover trends and patterns that can inform businesses, consumers, and the broader food industry.

<img src="https://assets.aboutamazon.com/dims4/default/e1f08b0/2147483647/strip/true/crop/1279x720+0+0/resize/1320x743!/format/webp/quality/90/?url=https%3A%2F%2Famazon-blogs-brightspot.s3.amazonaws.com%2Ff5%2F9f%2F43fe106c4a5081e7a696ef0a8fa8%2Ffresh-1280x7201.jpg" width="600">

### Dataset Background
The Amazon Grocery_and_Gourmet_Food Reviews dataset consists of reviews of Grocery_and_Gourmet foods from Amazon. The data span a period of more than 10 years, including all ~500,000 reviews. Reviews include product and user information, ratings, and a plaintext review.
The Amazon Grocery_and_Gourmet_Food Reviews dataset is a valuable resource to understand consumer behavior and the online review process. It is a large and comprehensive dataset that can be used to answer a variety of research questions.

##### Source of the Dataset : https://cseweb.ucsd.edu/~jmcauley/datasets/amazon_v2/
##### Description: 
To analyze the content of the reviews themselves and perform tasks like text classification, topic modeling, or sentiment analysis we use the text in the 'reviewText' column as the target variable.

The dataset contains the following columns:

            1) reviewerID - ID of the reviewer, e.g. A2SUAM1J3GNN3B
            2) asin - ID of the product, e.g. 0000013714
            3) reviewerName - name of the reviewer
            4) helpful - helpful votes of the review
            5) style - a disctionary of the product metadata, e.g., "Format" is "Hardcover"
            6) reviewText - text of the review
            7) overall - rating of the product
            8) summary - summary of the review
            9) unixReviewTime - time of the review (unix time)
            10) reviewTime - time of the review (raw)
            

### Research questions:

1. **Helpfulness Prediction:**
   - Predict how helpful a review will be based on the 'helpful' column using the content of the review text ('reviewText').
2. **Review Length and Ratings:**
   - Investigate the correlation between the length of a review ('reviewText') and the overall rating ('overall'). Do longer reviews tend to have higher or lower ratings?
3. **Reviewer Behavior:**
    - Identify patterns in reviewer behavior, such as frequent reviewers or those who tend to leave extreme ratings (very high or very low).
4. **Review Text Classification:**
     - Categorize reviews into specific topics or categories based on the content of the 'reviewText' column. For example, categorizing food reviews into different types of cuisine or product attributes.
5. **Temporal Analysis:**
     - Observe trends or patterns in review sentiment or review length over time using 'unixReviewTime' or 'reviewTime'.
6. **Reviewer Influence:**
    - Identify influential reviewers or reviewers whose opinions have a significant impact on product sales or ratings.
7. **Spam Detection:**
    - Develop a method to detect duplicate reviews or spam reviews that may artificially inflate or deflate product ratings.
8. **Comparative Analysis:**
    - Compare the sentiment and content of reviews for different products or brands within the dataset.

### Target Variable of the model : "reviewText"

### selected_features of the model = ['reviewText', 'reviewerID', 'reviewerName', 'asin', 'helpful', 'overall', 'summary', 'unixReviewTime', 'reviewTime']

### Goal : 
In this project I aim to employ natural language processing (NLP) techniques and sentiment analysis in conjunction with a machine learning model, utilizing both the textual content of the 'review text' and the numerical 'overall' rating columns, to classify reviews into distinct sentiment categories, namely positive, negative, or neutral. Also develop a collaborative filtering recommendation system using user-item interactions and latent factor modeling to generate personalized product ('asin') recommendations, leveraging historical review data and user preferences.
