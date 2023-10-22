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
  
- Research Questions:
 
  1. **Reviewer Behavior:**
     - Identify patterns in reviewer behavior, such as frequent reviewers or those who tend to leave extreme ratings.
  2. **Review Text Classification:**
     - Categorize reviews into specific topics or categories based on the content of the review text.
  3. **Spam Detection:**
     - Develop a method to detect duplicate reviews or spam reviews that may artificially inflate or deflate product ratings.

## Data

The Amazon Grocery_and_Gourmet_Food Reviews dataset consists of reviews of Grocery_and_Gourmet foods from Amazon. The data span a period of more than 10 years, including all ~151,254 reviews. Reviews include product and user information, ratings, and a plaintext review.
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

The EDA report offers a comprehensive understanding of the dataset, addressing missing values and duplicate rows while presenting vital statistics. EDA serves as the cornerstone for subsequent analysis, data cleansing, and modeling. Within the context of preparing the dataset for deeper analysis, I have conducted essential exploratory data analysis (EDA). This process sheds light on the data types within the dataset, which are fundamental for data manipulation and analysis. 

During this analysis, I have identified missing values in the dataset, with 'reviewerName' having 1,493 missing entries and 'reviewText' having 22. To rectify this, we imputed these gaps with appropriate placeholders: 'Unknown' for 'reviewerName' and 'No review available' for 'reviewText.' This adjustment ensures the dataset is more comprehensive and suitable for analysis without sacrificing valuable data. Furthermore, we verified the dataset for duplicate rows. The absence of duplicate rows is a positive discovery as they can skew the analysis and lead to inaccurate results.

##### Overall Distribution

| overall | overallPercentage | proportion |
|---|---|---|
| 0 | 5 | 57.81 |
| 1 | 4 | 21.55 |
| 2 | 3 | 11.58 |
| 3 | 2 | 5.23 |
| 4 | 1 | 3.82 |

![image](https://github.com/DATA-606-2023-FALL-TUESDAY/Edara_Manimadhuri/blob/main/src/Perc_Dist_Overall_rating.png)

##### A Scatterplot showing the relationship between overall rating and helpful votes: 
The graph indicates a right-skewed distribution of ratings, suggesting a greater number of products with higher ratings compared to those with lower ratings.   This is a positive sign since it indicates that consumers are delighted with the products they have purchased.
![image](https://github.com/DATA-606-2023-FALL-TUESDAY/Edara_Manimadhuri/blob/main/src/newplot.png)

#### Key findings from the EDA report:

- The overall rating of the products in the dataset is high, with an average rating of 4.24 out of 5.
- The most recent review was posted in July 2014.
- The median review was posted in February 2013.
- The distribution of the overall ratings is skewed to the right, with more products having higher ratings.
  
#### Text Preprocessing:

- Imported the necessary standard libraries, including Gensim for topic modeling, NLTK for text processing, and Matplotlib for visualization.
- Normalized the text by converting the 'reviewText' column to lowercase, to ensure that the text is consistent and not case-sensitive.
- Initialized a set of English stopwords using NLTK. These stopwords are common words like 'the,' 'and,' 'is,' etc., which are often removed from text data as they do not carry significant meaning.
- Defined a function preprocess_text to tokenize the text and remove stopwords. Which tokenizes the text, converts it to lowercase, and filters out non-alphabetic words and stopwords. The processed_documents list is created by applying the preprocess_text function to each document in the 'reviewText' column of the DataFrame.
- Defined another function, returning_tokinize_list, to tokenize all the words in the 'reviewText' column and combine them into a single list named tokenize_list_words for further analysis.

#### Topic modeling using Latent Dirichlet Allocation (LDA):
- Created a dictionary using the Gensim library. It associates words with unique integer IDs.
- Generated a corpus by converting each document into a bag of words. Each document is represented as a list of (word ID, word frequency) pairs based on the dictionary created earlier. This prepares the data for the LDA model.
- Performed LDA topic modeling using Gensim's LdaModel. It specifies the number of topics (in this case, 5) and uses the corpus and dictionary created earlier as input data. 
- We were further able to print the top words associated with each topic. For example, topic 0 is associated with words like 'coffee,' 'flavor,' 'cup,' and 'taste.'
  ![image](https://github.com/DATA-606-2023-FALL-TUESDAY/Edara_Manimadhuri/blob/main/src/wc1.png)

To assess the quality of the topics produced by the LDA model, a coherence score is calculated using the 'CoherenceModel'.   The coherence score quantifies the level of clarity and interpretability of the issues. Analyzing the recognized topics and their top words can offer significant insights into the content of the dataset, making it a useful technique for organizing and understanding text data.

#### Sentiment analysis using VADER(Valence Aware Dictionary and sEntiment Reasoner):

Conducting sentiment analysis on Amazon review data, explored the temporal evolution of sentiments in reviews. To achieve this, initiated the VADER sentiment analyzer and applied it to the 'reviewText' column in the DataFrame, assigning a sentiment score to each review. Subsequently, visualized the sentiment score distribution using a histogram. Later, converted the 'unixReviewTime' column to a datetime format and organized the data into time periods, in this case, monthly intervals. Calculating the mean sentiment for each period, generated a time series plot to visualize sentiment changes over time. This insightful analysis offers a deeper understanding of how sentiments evolve in Amazon grocery reviews, facilitating data-driven decisions and valuable insights.

![image](https://github.com/DATA-606-2023-FALL-TUESDAY/Edara_Manimadhuri/blob/main/src/senti_distribution.png)

Below graph shows that the average rating of the grocery store has declined over time. In 2001, the average rating was 0.9. In 2013, the average rating was 0.7.
This decline in average rating could be due to a number of factors, such as a decrease in the quality of the products or services, a spike in the number of negative customer reviews or a change in the demographics of the customers. 

Key insights from the graph:

- The decline in average rating is gradual, suggesting that it is not due to a single event or change.
- The decline in average rating is consistent across all years shown in the graph.
- The decline in the average rating is not uniform. The average rating declined more sharply between 2001 and 2003 than it did in subsequent years.

Overall, the image suggests that the grocery store has experienced a decline in customer satisfaction over time. These insights could be used to identify the root cause of the decline in customer satisfaction and develop strategies to address it.


![image](https://github.com/DATA-606-2023-FALL-TUESDAY/Edara_Manimadhuri/blob/main/src/senti_time.png)

 
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
