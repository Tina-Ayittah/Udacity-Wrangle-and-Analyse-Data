# Project 2-Wrangling and Analysing Data(WeRateDogs)


## Table of Contents
<ul>
<li><a href="#intro">Introduction</a></li>
<li><a href="#goal">Project Goal</a></li>
<li><a href="#overview">Project Steps Overview</a></li>
</ul>

<a id='intro'></a>
## Introduction
This project by Udacity requires one to use Python and its libraries to gather data from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it.

The purpose of this project is to show the wrangling skills i have learnt so far in Udacity Data Analyst Nanaodegree program. The dataset to be wrangled is the tweet archive of Twitter user @dog_rates(https://en.wikipedia.org/wiki/WeRateDogs), also known as WeRateDogs.

<a id='goal'></a>
## Project Goal
The main goal of this project is to effectively wrangle that is gather, assesss and clean [@WeRateDogs] for interesting nd insightful analysis and visualization


<a id='overview'></a>
## Project Steps Overview
### 1.Gathering Data
Three sets of data was gathered for this step. Twitter archive, image predictions and tweet_json.

NB: Before gathering the necessary libraries were imported.

twitter_archive_enhanced.csv: This was a file provided by udacity which was downloaded, uploaded to my workspace and read into a dataframe as twitter_archive_df.

image-predictions.tsv:By importing the python os and requests libraries this file was downloaded using the get function and url provided by udacity.Then read into a dataframe named image_predictions_df making use of read.csv and the separator.

tweet_json.txt: This additional data was obtained via my twitter developer account using the essential credentials and the code provided by udacity. After which the json file was read into and stored in a list then read into a dataframe twitterApi_df.

### 2. Assessing Data
Visual assessment: Each piece of gathered data is displayed in the Jupyter Notebook.Column headings explained.Additionally, each piece was asssesed in Excel.

Programmatic assessment: Pandas functions such as .head(), .info(), .describe(), .shape(), .duplicated(), .nuqiue(), .isnull(), . value_counts() and .loc() were used to assess each dataset programmatically.

After which the quality and tidiness issues of each dataset were documented.

### 3.Cleaning Data
Copies of each dataset was made before using the Define-Code-Test framework to clean each issue.

#### Quality

`twitter_enhanced_df`

For issues 1,2 and 3 the following columns (expanded_urls, in_reply_to_status_id, in_reply_to_user_id, retweeted_status_id, retweeted_status_user_id and retweeted_status_timestamp) were dropped.

For issues 4, 5 and 6 the appropriate code was used to change the rating numerator and denominator to float datatype and timestamp to datetime datatype and tweet id from int to string datatype.Also timestamp column was renamed to tweet_date.

For issue 7 I applied a code to find all the names with lower case from the name column and dropped them.

Issue 8: The invalid data in expanded url column of index number 2074 which is a picture of a human instead of a dog was dropped.

#9: Sources of tweets not cleary indicated the source column.

`image predictions`

#10: Changed tweet_id datatype to string

#11: Changed 'p1', 'p2', and 'p3' to lowercase

`twitterApi`

#12: changed data type for tweet id in twitterApi from int to object

#### Tidiness
#1:Converted the variable names (doggo, floofer, pupper,puppo) into a column and rename the column with the dog_stage
#2:Changed the column label from 'id' to 'tweet_id' in the twitterApi data(df2) dataset
#3: Merged the three data sets into one based on the tweet id.
**PS:out of the 12 data quality issues that were identified 5 identify as changing from one datatype to the other. Counting them as 1. In all 8 data quality issues were tackled.**

### Storing the Data
The merged data was saved in a csv file name twitter_archive_master.csv.

### Analyzing and Visualizing Data
The following insights and visualizations are deduced from three datasets; twitter archive, image 
predictions and tweet json which were wrangled and merged into a master data.
#### Insights
1. About 570 dogs that is 29% of dogs have no name.
2. The merged data has 21 rows and 1887 columns. All columns have no missing entries apart from the 
dog_stage.
3. Image number 1 is the most prominent 
4. The merged dataset has 21 columns and 1955 rows,
5. All the rows except for the dog stage column are completely filed with no missing value.
6. The columns are 'tweet_id', 'tweet_time, 'source', 'text', 'expanded_urls', 'rating_numerator', 
'rating_denominator', 'name', 'stage', 'retweet_count', 'favorite_count', 'jpg_url', 'img_num', 
'p1', 'p1_conf', 'p1_dog', 'p2', 'p2_conf', 'p2_dog', 'p3', 'p3_conf', 'p3_dog'
#### Visualizations
Visual can be found in .ipynb and the act report