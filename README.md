# Yelp-Data-Set-Analysis
Analyze Yelp Data Set using Python


Methods and Analysis:

First, our group successfully downloaded a dataset from https://www.yelp.com/dataset/challenge. Though the dataset is quite large, comprising of 6,685,900 reviews for 192,609 businesses in 10 metropolitan areas, it is merely a sample of Yelp’s entire catalogue. This dataset is designed primarily for student use. The non-pictured data is 3.6 gigabytes compressed, and 8.69 gigabytes uncompressed.
On Python, we imported TextBlob and pandas, and we also ran the code "from sklearn.model_selection import train_test_split". This imported is a classifier comparison module that allows data with several dimensions to be more easily analyzed (Classifier Comparison).
We then assigned review to the appropriate json file, and set our “chunksize” to 1000 ("review = pd.read_json('review.json',lines=True, chunksize=1000)"), which means we instructed Python to only read 1000 rows of data at a time. We picked 1000 because it is still a large set of data, but not so large that it impacted performance.
Next, we set a for-loop to read each row individually, and we set the shape of the outputted data. From here, we were able to examine the first and last 30 rows of varying combinations of data, from “Cool”, “Funny”, and “Useful” votes for individual reviews, to number of stars in each review, to the user ID and business ID of the review, and to the actual text of the review. From this module, we are also able to call the text from individual reviews and display the results as output.
Finally, we were able to examine the metadata from this chunk of 1000 reviews. Notable datapoints we were able to produce include the mean “Cool”, “Funny”, and “Useful” votes on each review, the mean star rating for the 1000 reviews, standard deviation for each of these metrics, and 25th, 50th, and 75th percentile marks in ascending order for these reviews.
Conclusions
It should be noted that the mean number of “Cool” votes for each review was 0.524000, while the mean amount of “Funny” votes was 0.452000, and the mean amount of “Useful” votes was 1.271000. What is most telling is that these metrics have very long tails. The 50th percentile for each of these metrics is 0. The 75th percentile “Cool” review had only 1 vote; the 75th percentile “Funny” vote was 0; the 75th percentile “Useful” vote was only 1. The max amount for each was 15 “Cool” votes, 14 “Funny” votes, and 23 “Useful” votes. Since our means were all larger than the 50th percentile for each metric, our largest values had a very significant impact on each mean.
Our mean star rating was 3.654000, with a 50th percentile measure of 4.0. Thus, very low ratings of 1 star had a significant impact on the mean.
