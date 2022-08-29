# We-Rate-Dogs
## by Moyinoluwa Busola Agbaje


## Dataset

#### Introduction:

- This project illustrates the data wrangling process for the tweet archive of Twitter user @dog_rates also known as WeRateDogs, which is also the dataset I used in the entire wrangling, analyzing and visualizing process. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. In this wrangling and analysis, I ilustrated the data wrangling techniques that were used to gather, assess and clean the dog twitter archive.

#### Data Gathering:
For the analysis and wrangling, the following files were gathered:
- The WeRateDogs (@dog_rates) Twitter archive - This file (archive.csv) was downloaded using Twitter's API and consists of basic tweet data for 2300+ tweets from WeRateDogs.
- The tweet image predictions - that is, the kind of breed a dog is (or other object, animal, etc.), that is present in each tweet according to a neural network. The file, image_predictions.tsv, was downloaded programmatically from Udacity.
- Each tweet's retweet_count and favorite_count - This file (tweet_json) contains JSON data for each tweet indicating the retweet and favorite counts.

#### Data Assessing:
- I loaded the three (3) files that were obtained in the gathering phase, and singly fed them into the Pandas data frames for assessment. Both visual and programmatic evaluation was done for each of the data frame.

#### Data Cleaning:
The quality and tidiness issues were cleaned using programmatic techniques such as:
- Removing rows that had null retweets.
- Removing rows with duplicated information.
- Deleted rows that had no dog predictions at all.
- Combining all the three data frames into a single data frame.

## Summary of Findings

- 181 retweets present but we are only interested in original tweets.
- There are 78 reply Tweets, we’re only interested in “original Tweets”.
- Missing values in columns: in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp, and expanded_urls in the twitter_archive Table.
- Some uppercase and lowercase letters identified in columns 'p1', 'p2', and 'p3' in the image_prediction Table.
- Removed the 'source' column in the twitter_archive Table.
- Dropped rows with duplicates in the jpg_url column.
- Changed timestamp format from "2017-07-26 15:59:51+00:00" to "2017, 2016, 2015...
- The column 'id' was changed to tweet_id in the newapi Table.
- Some tweets have wrong values extracted for rating and some text contains the Tweeter's rating.
- Some tweets with rating_denominator NOT equal to 10; multiple dogs or no valid rating.
- There are 5 tweets with rating_numerator >= 15, which either don't make sense or are huge.