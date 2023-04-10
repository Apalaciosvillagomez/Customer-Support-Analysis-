![Logo](https://camo.githubusercontent.com/7bf6f8c804cf1ec62e2cbbc7c85ea7dfd65b4848df48be4218e24012c6eb3430/68747470733a2f2f692e6d6f72696f682e636f6d2f323032302f30322f30342f6265656633366664373037642e6a7067)

# Customer Support Analysis

The sentiment analysis model aims to solve the real-world problem of tracking and analyzing customer feedback for businesses. Customer complaints and negative sentiment can have a significant impact on a company's reputation and bottom line. By identifying the top 10 companies with the most complaints, stakeholders can proactively address the underlying issues that are leading to negative feedback and improve the overall customer experience.

## What are we aming to solve?

We are looking to help businesses understand how their customers feel about their products, services, or brand in general. By analyzing the sentiment of customer tweets, businesses can gain insights into what customers like or dislike about their offerings.

This information can then be used to improve their products or services to better meet customer needs and preferences. Additionally, sentiment analysis can help businesses identify customer complaints or negative feedback early on, allowing them to respond quickly and resolve issues before they escalate.

Furthermore, sentiment analysis can be used to track the success of marketing campaigns or product launches. By monitoring sentiment over time, businesses can gauge whether their efforts are resonating with customers and adjust their strategies accordingly.

Overall, a Twitter sentiment analysis for customers can help businesses make more informed decisions, improve customer satisfaction, and ultimately drive business growth. 

## Overview 

In this project we will be celaning, formating and processing data in order to meet our objectives and give valuable and meaningfull insights such as:

- Top 5 companies with tweet complaints
- Avg response time by company
- Sentiment change after interaction with company

### Steps

1-. Retreive data

2-. Analyze data

3-. Download Pkgs 

4-. Process Data (Format data as requiered)

6-. Create Model 

7-. Evaluate Model.

## Data set 
 We will work with the following data set wich contains more than 1 millon rows and the following featuers:

    - tweet_id : A unique, anonymized ID for the Tweet. Referenced by response_tweet_id and in_response_to_tweet_id.

    - author_id : A unique, anonymized user ID. @s in the dataset have been replaced with their associated anonymized user ID.

    - inbound : Whether the tweet is "inbound" to a company doing customer support on Twitter. This feature is useful when re-organizing data for training conversational models.

    - created_at : Date and time when the tweet was sent.

    - text : Tweet content. Sensitive information like phone numbers and email addresses are replaced with mask values like email.

    - response_tweet_id : IDs of tweets that are responses to this tweet, comma-separated.

    - in_response_to_tweet_id : ID of the tweet this tweet is in response to, if any.

### Initial Data View
![initial data view](https://user-images.githubusercontent.com/115577909/230841679-6a03b445-e749-4163-ac53-4f61c221830f.PNG)


## Cleaning Data
![image](https://user-images.githubusercontent.com/115577909/230843134-23aea61b-aedb-45c1-81cf-3231e9532ae4.png)
This step is an essential step in preparing data for sentiment analysis of tweets. The following are some steps involved in the data cleaning process:

    - Removing irrelevant information such as URLs, mentions, hashtags, emojis, and special characters.
    - Removing stop words such as "and", "the", "a" etc.
    - Correcting misspelled words using algorithms or dictionaries.
    - Standardizing abbreviations and slang words.
    - Handling negations, such as "not good" or "not happy".
    - Removing duplicates and irrelevant tweets.
    - Converting all text to lowercase or uppercase for consistency.
    
By performing these steps, the resulting data is cleaned and ready for further analysis to extract meaningful insights from the tweets.

# Model

## Top 5 companies with tweet complaint

For this first insight we were able to use our clean data to creat a value count for teh companys and were able to retreive tyhe top 5 companies wityh most complaints, these will also be the companies in wich our analysis will be based.
