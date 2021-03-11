# We Rated Dogs - Data Wrangling

## Introduction
Real-world data rarely comes clean. Here, the main goal is to wrangle **"WeRateDogs"** Twitter data to create interesting and trustworthy analyses and visualizations. 
Using **Python** and **its libraries**, I gather data from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it.
.

## What is "We Rated dogs"?
Is a Twitter account that rates people's dogs with a humorous comment about the dog.

## Information about the project
Only one file is provided: a csv document with 17 columns and 2356 rows from which information is provided such as:
- **tweet_id**: the unique identifier for each tweet
- **in_reply_to_status_id**: if the represented Tweet is a reply, this field will contain the integer representation of the original Tweet’s ID
- **in_reply_to_user_id**: if the represented Tweet is a reply, this field will contain the integer representation of the original Tweet’s author ID
- **timestamp**: time when this Tweet was created
- **source**: utility used to post the Tweet, as an HTML-formatted string. e.g. Twitter for Android, Twitter for iPhone, Twitter Web Client
- **text**: actual UTF-8 text of the status update
- **retweeted_status_id**: if the represented Tweet is a retweet, this field will contain the integer representation of the original Tweet’s ID
- **retweeted_status_user_id**: if the represented Tweet is a retweet, this field will contain the integer representation of the original Tweet’s author ID
- **retweeted_status_timestamp**: time of retweet
- **expanded_urls**: tweet URL
- **rating_numerator**: numerator of the rating of a dog. Note: ratings almost always greater than 10
- **rating_denominator**: denominator of the rating of a dog. Note: ratings almost always have a denominator of 10
- **name**: name of the dog
- **doggo**: one of the 4 dog "stage"
- **floofer**: one of the 4 dog "stage"
- **pupper**: one of the 4 dog "stage"
- **puppo**: one of the 4 dog "stage"

Through an **API created by code**, data is obtained **from Twitter** to complement the previous file. This data is transformed into a DataFrame which contains: 

- **id**: the unique identifier for each tweet
- **retweet_count**: number of times this Tweet has been retweeted
- **favorite_count**: indicates approximately how many times this Tweet has been liked by Twitter users

Finally, a document is **downloaded by code (from Udacity servers)**, to complement the previous ones. This document corresponds to information on predictions about 
the breed of the dog analyzed in each twitter. It contains the columns:

- **tweet_id**: the unique identifier for each tweet
- **jpg_url**: dog's image URL
- **img_num**: the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images)
- **p1**: algorithm's #1 prediction for the image in the tweet
- **p1_conf**: how confident the algorithm is in its #1 prediction
- **p1_dog**: whether or not the #1 prediction is a breed of dog
- **p2**: algorithm's #2 prediction for the image in the tweet
- **p2_conf**: how confident the algorithm is in its #2 prediction
- **p2_dog**: whether or not the #2 prediction is a breed of dog
- **p3**: algorithm's #3 prediction for the image in the tweet
- **p3_conf**: how confident the algorithm is in its #3 prediction
- **p3_dog**: whether or not the #3 prediction is a breed of dog


The objective of the project **isn't to leave a 100% functional database on dogs**, but to show **how create an API** to obtain information from twitter and the **code and techniques to gather, assess and clear the data**.
