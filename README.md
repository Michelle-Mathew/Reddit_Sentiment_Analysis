# Reddit_Sentiment_Analysis
The code pulls top level comments of the recent 250 discussion threads from the popular subreddit r/wallstreetbets in order to conduct a sentiment analysis for each post.
All data is placed in a dataframe.
The code starts off by separating the emojis and text from each comment. Unwanted characters are removed from the text and words are lemmatized to its root form.
Then a list of stocks is created using data from the website-> https://swaggystocks.com/dashboard/wallstreetbets/ticker-sentiment.
Looping through the list of stocks, the code calculates the frequency of stocks mentioned under each post.
Using the LoughranMcDonald_MasterDictionary updated with popular reddit terms and an emoji dictionary sentiment scores are calculated for each post.
Taking the top 5 mentioned stocks across the sample(done manually); Quandl is used to pull trading data for the top 5 stocks.
A linear regression analysis was done for Total Sentiment scores (emoji + text), Emoji Sentiment and Text Sentiment scores. Abnormal Returns were used as the dependent
variable. This is to test the hypothesis if the sentiment on reddit could predict abnormal returns of a given stock. Lag returns were added to see if it would 
improve the model.
Lastly, a cross-section regression analysis was done across the top 5 stocks to test the hypothesis. 
