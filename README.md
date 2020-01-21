
README

This is a simple machine learning program using matplotlib, numPy, Pandas, and skLearn, it uses a webscraper to scrape the s&p500 tickers from the wikipedia page on the s&p 500 found here: https://en.wikipedia.org/wiki/List_of_S%26P_500_companies.

Then, the scaper file uses the list of tickers to interact with the yahoo finance api to grab the stock data of each ticker based on dates that can be edited in the scaper file. Each ticker has a csv file created filled with data from date A to date B. The data is then fed into the compile_data() function where the joined closes are combined into one large excel file (joined closes are used to account for price differences that may occurr from stock splits).

This csv file is calle dthe sp500_joined_closes.csv, it is used for the machine learning side of this project. The data is processed, the feature-sets are extracked and fed into the machine learning algorithm where voting classifiers are used to decide weather to buy, sell, or hold the stock. I am using 3 classifiers, LinearSVC, KNeighborsClassifier(), and RandomForestClassifier(). The data from the ML algorithm returned gives you the amount of votes from each classifier as well as a -1,0, or 1. 

-1 means to sell
0 means to hold
1 means to buy

The confidence score is the percentage at which all 3 votingclassifiers are based in terms of confidence for the decision being provided. This project is a work in progress and will be updated.
