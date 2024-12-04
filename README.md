# Sentiment Analysis
This project focuses on Sentiment Analysis of text reviews using Natural Language Processing (NLP) techniques, complemented by visualizations such as WordClouds for a pictorial representation of the textual data. By analyzing the content, the project aims to determine whether a given review conveys a positive, negative, or neutral sentiment. The process involves cleaning, preprocessing, and visualizing the data, followed by leveraging sentiment analysis tools like VADER (Valence Aware Dictionary and sEntiment Reasoner) to classify and interpret the text accurately.

## Installation
- pip install nltk :To install the NLTK (Natural Language Toolkit) library for NLP tasks

- pip install wordcloud : For generating word clouds

```
pip install nltk
pip install wordcloud
pip install matplotlib
pip install seaborn
pip install pandas
pip install numpy
pip install textblob
```

## Dataset Descriptions
The dataset is related to ```app reviews```, where users provide feedback about a specific application.This dataset provides rich information for analyzing user feedback, app performance, and developer interactions. Its diverse columns make it suitable for tasks such as sentiment analysis, user behavior study, and feature evaluation.  
The dataset consists of ``` 16,787 rows and 12 columns ```, each capturing various aspects of user reviews for an app. Below is a detailed summary of the columns:

**`reviewId`**: A unique identifier assigned to each review.    
**`userName`**: The name of the user who submitted the review.  
**`userImage`**: The URL linking to the user's profile image.   
**`content`**: The actual text of the review written by the user.   
**`thumbsUpCount`**: The number of likes or "thumbs up" the review received from other users.   
**`reviewCreatedVersion`**: The version of the app reviewed by the user (may contain missing values).   
**`at`**: The date and time when the review was submitted.                  
**`replyContent`**: The developer's reply to the review (if applicable; many values are null).  
**`repliedAt`**: The date and time when the developer replied to the review (if applicable).    
**`appVersion`**: The version of the app used by the reviewer at the time (may contain missing values).     
**`sortOrder:`**: Indicates the sort order of the reviews (e.g., "most_relevant").   
**`appId`**: The unique identifier of the app (e.g., "com.anydo").
**`appId`**


## Importing Dataset

```
df = pd.read_csv(r"File_path")
```

## Data Preprocessing

1. Data Cleaning:
Converts text to lowercase.
Removes links, numbers, special characters, and extra spaces.
Handles missing values.

2. Text Preprocessing:
Tokenization: Splits text into words.   
Stopword Removal: Eliminates common words (e.g., "the", "and") using NLTK.      
Stemming: Reduces words to their base form using PorterStemmer. 
Lemmatization: Converts words to their dictionary form using WordNetLemmatizer.


3. Sentiment Analysis:
VADER: Used for determining the sentiment polarity (positive, negative, neutral).
TextBlob: Provides additional polarity scoring for comparison.


4. Visualization:


WordClouds:
Represents the most frequent words across all reviews.
Separate WordClouds for positive, negative, and neutral reviews.
Charts and Graphs: Displays sentiment distribution and other key trends.

## Word Cloud Generation
- Word Cloud Generation is a visualization technique used to represent the frequency of words in textual data.Configurations such as width, height, background color, and maximum words are applied to customize the appearance.

![Word Cloud Generation](https://github.com/user-attachments/assets/d795a575-0e2a-4486-b5f1-3fb212b5217e)




## Sentiment Analysis with VADER

Sentiment Analysis with VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon-based sentiment analysis tool specifically designed to analyze text for sentiment polarity and intensity. In this project, VADER is employed to classify user reviews into positive, negative, or neutral sentiments based on their content.

## Sentimental Classification
### Using VADER Sentiment Analysis:
VADER (Valence Aware Dictionary and sEntiment Reasoner) is commonly used for text sentiment analysis, especially for social media or short-form content like reviews.   
VADER assigns a "compound score" to each review or text, which is a combination of the positive, negative, and neutral scores.
#### Positive Sentiment:
 When the compound score is greater than 0.05, the text is classified as positive.
 #### Negative Sentiment: 
When the compound score is less than -0.05, the text is classified as negative.
#### Neutral Sentiment: 
When the compound score is between -0.05 and 0.05, the text is classified as neutral.

## Pictorial representation

- Provide an intuitive overview of common words in all reviews.
- Generate separate WordClouds for positive, negative, and neutral reviews to highlight key themes associated with each sentiment.

![positive Representation](https://github.com/user-attachments/assets/bf715ad7-19e4-40bd-8f4a-6a9b1bc39a8d)

![Negative Representation](https://github.com/user-attachments/assets/013be014-ad19-46c2-9d47-9fb0dd6ab429)

![Nuetral Representation](https://github.com/user-attachments/assets/ed5faba4-e869-43de-9fd1-26f9ff92c1a3)



## Bar Chart for Sentiment Distribution

![Bar Chart](https://github.com/user-attachments/assets/0510d9ff-3f4c-46db-9fe0-c97b6940183c)            

## Top 10 Frequent Words

![Top 10 Frequent Words](https://github.com/user-attachments/assets/5adabacb-6ec8-4c6d-ac88-964f9f2001ae)

  





