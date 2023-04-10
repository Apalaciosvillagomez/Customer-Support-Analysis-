![Logo](https://camo.githubusercontent.com/7bf6f8c804cf1ec62e2cbbc7c85ea7dfd65b4848df48be4218e24012c6eb3430/68747470733a2f2f692e6d6f72696f682e636f6d2f323032302f30322f30342f6265656633366664373037642e6a7067)

# Customer Support Analysis

The sentiment analysis model aims to solve the real-world problem of tracking and analyzing customer feedback for businesses. Customer complaints and negative sentiment can have a significant impact on a company's reputation and bottom line. By identifying the top 10 companies with the most complaints, stakeholders can proactively address the underlying issues that are leading to negative feedback and improve the overall customer experience.

## What are we aiming to solve?

We are looking to help businesses understand how their customers feel about their products, services, or brand in general. By analyzing the sentiment of customer tweets, businesses can gain insights into what customers like or dislike about their offerings.

This information can then be used to improve their products or services to better meet customer needs and preferences. Additionally, sentiment analysis can help businesses identify customer complaints or negative feedback early on, allowing them to respond quickly and resolve issues before they escalate.

Furthermore, sentiment analysis can be used to track the success of marketing campaigns or product launches. By monitoring sentiment over time, businesses can gauge whether their efforts are resonating with customers and adjust their strategies accordingly.

Overall, a Twitter sentiment analysis for customers can help businesses make more informed decisions, improve customer satisfaction, and ultimately drive business growth. 

## Overview 

In this project we will be cleaning, formatting and processing data in order to meet our objectives and give valuable and meaningful insights such as:

- Top 5 companies with tweet complaints
- Avg response time by company
- Sentiment change after interaction with company

### Steps

1-. Retrieve data

2-. Analyze data

3-. Download Pkgs 

4-. Process Data (Format data as required)

6-. Create Model 

7-. Evaluate Model.

## Data set 
 We will work with the following data set which contains more than 1 million rows and the following features:

    - tweet_id : A unique, anonymized ID for the Tweet. Referenced by response_tweet_id and in_response_to_tweet_id.

    - author_id : A unique, anonymized user ID. @s in the dataset have been replaced with their associated anonymized user ID.

    - inbound : Whether the tweet is "inbound" to a company doing customer support on Twitter. This feature is useful when re-organizing data for training conversational models.

    - created_at : Date and time when the tweet was sent.

    - text : Tweet content. Sensitive information like phone numbers and email addresses are replaced with mask values like email.

    - response_tweet_id : IDs of tweets that are responses to this tweet, comma-separated.

    - in_response_to_tweet_id : ID of the tweet this tweet is in response to, if any.

### Initial Data View

<div align="center">
    <img src= "https://user-images.githubusercontent.com/115577909/230841679-6a03b445-e749-4163-ac53-4f61c221830f.PNG">
</div>


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

For this first insight we were able to use our clean data to create a value count for the companies and were able to retrieve the top 5 companies with most complaints, these will also be the companies in which our analysis will be based.


<div align="center">
    <img src= "https://user-images.githubusercontent.com/115577909/230843753-d0719100-2eaa-48f5-b134-a77a9d39e1fb.png">
</div>

### Findings

  From the table above its safe to say that AmazonHelp is the company with most complaints.

## What day of the week do more complaint come in?

In order to find this we will work with our created_at featuer and work with the pkg "Seaborn", this model will be of help for companies to know what day of the week more resources are going to be needed.

<div align="center">
    <img src= "https://user-images.githubusercontent.com/115577909/230845703-16966c1e-e50e-4477-b31b-95d72ddc8c13.png">
</div>

### Findings

  It's clear that Fridays being the first weekend day is the day with most complaints.

## Avg response time by company

In this model we will be working with a created dataframe in wich we have created a new Column called "response_time" this will help us average all the tweets the companys have answered.

<div align="center">
    <img src= "https://user-images.githubusercontent.com/115577909/230848267-77ed7a5d-8aa3-46f6-a91f-cc37e5cddce8.png">
</div>

### Findings

  Although between our Avg response times there isn't a great gap we can see that Verizon Supports team has the fastest response time being an Avg of 3.61 minutes
  
## Sentiment Analysis 

Here we are going to see the base of this project, we will be able to see what the client's initial sentiment was and the change in sentiment after interacting with Customer Support, we will also see the sentiment in the companies tweets; this will help the companies know what type of sentiment the change in their clients and create strategies to have a more relevant change in said sentiment.

<div align="center">
    <img src= "https://user-images.githubusercontent.com/115577909/230850250-83f0fc82-5fe5-4c73-8c00-d5840c92cd03.png">
</div>

### Findings

 We can see by the sentiment analysis shown that nationalrailenq was the company with the most change in sentiment, although there where changes in sentiment, none of them quite came out one the positve side, this should be a key indicator for companies to focus on working on their customer support team.



## Sources and references

### Dataset

The following link will take you to the download page for the Dataset used for this model https://www.kaggle.com/datasets/thoughtvector/customer-support-on-twitter
  -In order to download click on the botton "download" located on the top right corner, after the download is complete yopu must unzip the file and the dataset will be    ready to use.

### Sources

The following links are some references that helped create the model please visit in case of any doubt:

 - https://stackoverflow.com/a/43023503/3971619
 - https://www.kaggle.com/sudalairajkumar/getting-started-with-text-preprocessing
 - https://github.com/NeelShah18/emot/blob/master/emot/emo_unicode.py
 - https://www.machinelearningplus.com/nlp/topic-modeling-gensim-python/
 - https://stackoverflow.com/questions/46282473/error-while-identify-the-coherence-value-from-lda-model

### Non-technical Presentation

A non-technical poresentation was created to better understand the buisiness side of the present project, you can find the presentation on the following:

https://github.com/Apalaciosvillagomez/Customer-Support-Analysis-/blob/9326cad73fb339eec68e13246e9df06a853e79af/Non-technical%20Presentation.pdf

# Repository Exploration

1-. Capstone Project Proposal.pdf [file]
 In this pdf you can view the proposal for this project.
 https://github.com/Apalaciosvillagomez/Customer-Support-Analysis-/blob/f1ecbc009d04d20affe2f133e2107a7091e92991/Capstone%20Project%20Proposal.pdf

2-. Customer Support Notebook.ipynb [model/main notebook]
 This is the notebook that contains the whole project, from data exploration
 
 https://github.com/Apalaciosvillagomez/Customer-Support-Analysis-/blob/f1ecbc009d04d20affe2f133e2107a7091e92991/Customer%20Support%20Notebook.ipynb

3-. Non-technical Presentation.pdf [file]
 Here you can find the slide for the Non-technical presentation.
 https://github.com/Apalaciosvillagomez/Customer-Support-Analysis-/blob/2df305cdad83a4006d2d519d4b181c932f96ebc3/Non-technical%20Presentation.pdf

4-. README.md [file]
 file you are currently reading 
 
5-. Twitter Complaints Dataset
 This is where you can find instructions to download the dataset used for this project.
 https://github.com/Apalaciosvillagomez/Customer-Support-Analysis-/blob/2df305cdad83a4006d2d519d4b181c932f96ebc3/Twitter%20Complaints%20Dataset
 
 
