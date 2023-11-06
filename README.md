![image](https://github.com/Seanabuklau/Text_Mining/assets/66303787/4323c84e-1153-4cb3-a053-8175353d429b)![image](https://github.com/Seanabuklau/Text_Mining/assets/66303787/0b766aef-a95e-4d2a-996a-b635ec348b59)# Text_Mining

## Introduction
This project was done as part of a text mining assignment. The task was to use the News Category Dataset from Kaggle and come out with 3 business questions that can be answered using this analysis, as well as potential benefits that can be yielded as an end user. 

## Business Questions

### 1. How can marketing companies or departments better target audience and customers about existing or upcoming product launches? 
Generally, news articles tend to report on current affairs or publish opinion pieces based on public sentiments or predicted behaviours. Therefore, by tracking and identifying popular and relevant news topics, organizations can create timely and engaging content that resonates well with their audience. This helps to increase better brand visibility and increase engagements with an organisation’s products. 

### 2. How can banks and financial institutions stay ahead of the market and make strategic investment decisions? 
Investment firms and traders can track news headlines to inform their trading strategies and investment decisions. Monitoring financial news for information on market trends, economic indicators, corporate earnings reports, and geopolitical events that can impact stock prices and other asset classes. Thus, by tracking news data closely, this can help financial professionals identify buying and selling opportunities, manage risk, and adjust portfolios in response to breaking news. 

### 3. How do companies gain insights into their competitor’s activities and strategies in order to out-perform them? 
Companies are always on the look out for new competition in the market. One way to assess competing companies is to ascertain the strengths and weaknesses of current and potential competitors. This strategy can help companies learn the ins and outs of how their competition work, and identify potential opportunities where they can out-perform them. 

## Methodology

### Business Question 1 - Topic Modelling
For the scope of this project, the focus will be on helping Food & Beverage companies market their products better by understanding F&B trends over the past decade. A proposed methodology for doing so is to use Topic Modelling to identify hidden topics or themes that occur within news descriptions, so that companies can learn and make better marketing ads or campaigns in future. 

Latent Dirichlet Allocation (LDA) was the method used for topic modelling, where this approach uses a generative probabilistic model for collections of discrete data, such as text corpora. It assumes that each document is a mixture of topics, where each topic is characterized by a distribution over words, and the goal of LDA is to infer the topic distributions of the documents in a corpus.

Here, LDA was used to extract topics from the news dataset, where the top 20 words for the top 10 topics among the entire dataset was yielded. To visualise the results, WordCloud library was used to visualise the dominant keywords, where they represent F&B trends over the past decade.

### Business Question 2 - Sentiment Analysis
For the scope of this project, the focus would be analysing business news, where the assumption is that this data reflects market sentiments. A proposed methodology for doing so is using Sentiment Analysis to understand the markets better, where a positive sentiment can mean a bullish market and conversely a negative sentiment can mean a bearish market. 

VADER sentiment analyser was used for sentiment analysis. This technique is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media. VADER works by assigning a sentiment score to each word in a text. The scores are then summed to get a sentiment score for the entire text. VADER takes into account the context of the words, such as negations and intensifiers, to get a more accurate sentiment score.

Sentiment analysis with VADER was applied on each news article, and then further processed to get the average sentiment per year in numbers. The assumption here is that a positive sentiment i.e. >0 means a bullish market and a negative sentiment i.e. <0 means a bearish market. The results were visualised using AutoViz and Matplolib libraries to display the sentiments of business news data throughout the decade.

### Business Question 3 - Entity Recognition
For the scope of this project, the focus would be assessing Apple as a competitor in the tech and mobile marketplace. A proposed methodology for doing so is to use Named Entity Recognition (NER), which can help  to track news and events relating to Apple Inc.

NER is a subtask of information extraction that helps to locate and classify named entities mentioned in unstructured text into pre-defined categories such as person names, organizations, locations, etc.

in this case, NER was used to extract articles that contain Apple related terms like iPhone, iOS, Cupertino, etc. The results are output in a pandas Dataframe with the corresponding keywords and link to the news articles that contain them. Furthermore, a bar-chart visualisation was also created where the x-axis is the top keywords and the y-axis comprised the corresponding article links of those articles containing such keywords. 
