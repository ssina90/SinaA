# Using AI to detect news sentiment to predict changes in stock prices
(Last updated 10/3/21)

## Introduction 
Our goal is to design a script in which it gathers news articles for a particular stock or stocks throughout the day and use sentiment analysis to see whether a stock is good to buy or to sell. Exactly what is Sentiment Analysis? Simply it is a machine learning tool that analysis groups of text or words and check if these phrases condone a positive or negative sentiment. 

The project will have three parts to it, the first part is to create a web scrapper that gets and gathers articles on a particular stock, the second part will be where we use the articles that we find and perform sentiment analysis on them and lastly, the third part will be based on our results for part two, use that to buy or sell our shares. 

## Part 1: Gathering our articles 
Firstly we need to scrap our articles from the internet. To do this we are using FinViz a website that shows stock data and is free which is easily accessible to users. We are concerned with indiviudal stocks thus we have to get the articles on a specific stock, luckly FinViz list articles based on the stock. As seen below, the code gathers all the html information that we need from the website. The data is stored in a dictionary with the key being the stock ticker, as we want to group them buy specific stocks.   

![](/images/pic1.png)

Our next code chuck, extracts the speicifc information we need from the website or html file, we are not interested in the specifics of the code, all we want is the date, and link of the article and we group them by the articles date. 

![](/images/pic2.png)

Now, this is the interesting part of our project, going through invidiual links and just getting the article paragraphs. An interesting code that was done here to do this was the code at line 8 below. Was this does it grabs all the text within the html file that is in a paragraph, and then converts them to a string. We store all these articles in a list. 

![](/images/pic3.png)

## Part 2: Conducting Sentiment Analysis

Now that we have all the data we need to conduct our Sentiment Analysis, we want to first store it in 
