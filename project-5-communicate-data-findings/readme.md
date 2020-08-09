# WeRateDogs Data Exploration

## Dataset

-This data set contains information about 1300 dogs collected from the tweet archive of Twitter user @dog_rates, also known as WeRateDogs and The tweet image predictions
### Sources:
- Download `twitter_archive_enhanced.csv` directly and import it using pandas.read_csv function, which is hosted on Udacity's servers.
- Download `image_predictions.tsv` programmatically using the <a href="https://pypi.org/project/requests/">Requests</a> library and the following URL: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv ,and import it using pandas.read_csv function, which is also hosted on Udacity's servers.
- Using the tweet IDs in `twitter_archive_enhanced.csv`, query the Twitter API for each tweet's JSON data using Python's <a href="http://www.tweepy.org/" >Tweepy</a> library and store each tweet's entire set of JSON data in a file called `tweet_json.txt` ,then read the file and, create a new dataframe using pandas and append JSON data in it.
- the data has been assessed and cleaned, and finally gathered in one csv file `twitter_archive_master.csv`  


## Summary of Findings

In the exploration,
I started to univariate exploration, as for categorical variables i started asking these questions:
- The Distribution of Breeds of Dogs, how can i represent all the breeds ,so i found it is better to focus on the top 10 breeds 
- The Distribution of Stages of Dogs compare to unclassified dogs
- The Distribution of Prediction Algorithms and which is the most used algorithm
- The Distribution of Images Number and  which image is most used to predict the breed of dog
- The Distribution of Times of Day, when did most of the tweets are posted 

after that i focus on the numerical variables:
- Retweet Count Distribution, how is the count is distributed, log scale and set new bins will be a good solution for highly skewed distribution
- Favorite Count Distribution, same as retweet count
- Rating Numerator Distribution, limit x-axis and set new bins will be good solution to highly skewed distribution

then i started bivariate exploration:
- Average Confidance for Prediction Algorithms and related it to The Distribution of Prediction Algorithms (barplot)
- Average Confidance for Image Number and related it to The Distribution of Images Number (barplot)
- Prediction Algorithms and Image Number, how the distribution of these two varibles are related to each other (countplot)
- Relation between `Retweet Count` and `Favorite Count` (scatterplot)
- Relation between `Retweet Count` and `Times of Day` (boxplot, violinplot, and histogram grid)
- Relation between `Favorite Count` and `Times of Day` (boxplot, violinplot, and histogram grid)
- Relation between `Retweet Count` and `Stages of Dogs` (boxplot and violinplot)
- Relation between `Favorite Count` and `Stages of Dogs` (boxplot and violinplot)

finally, multivariate exploration:
- Average Confidance corresponding to Prediction Algorithms and Image Number, how is the relation between these three variables
- Times of Day corresponding to Retweet Count and Favorite Count
- Stages of Dogs corresponding to Retweet Count and Favorite Count

## Key Insights for Presentation

For the presentation,
- we will present all the univariate exploration with comments for both categorical and numerical variables.
- as for bivariate exploration, we want to see how :
* Average Confidance for Prediction Algorithms is related to The Distribution of Prediction Algorithms and what observations about each algorithm
* Average Confidance for Image Number is related to The Distribution of Images Number and which image has the highest average confidance
* Prediction Algorithms and Image Number, how these two varibles are related to each other
* Relation between `Retweet Count` and `Favorite Count` (histogram) to see the relation between these two variables
- finally, as for multivariate exploration, i focused on Average Confidance corresponding to Prediction Algorithms and Image Number, to see the relation between these three variables 
