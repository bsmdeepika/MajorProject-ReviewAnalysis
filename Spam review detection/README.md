# Fake Reviews Detection

We collected multiple layers of Amazon product and review data to identify fake reviews. In this repo you will find two notebooks that contain Python code to do:
1. Cleaning data: the data we get from scraping aren't yet ready to be analyzed, so we did several data cleaning steps
2. Generate new attributes for analysis: two new attributes, sentiment_score and most_rev, were generated to do more in-depth analysis

In addition, in `final_dataset` folder, you will find the cleaned final dataset for further analysis.


## Project Summary
Developed approach to identify fake reviewers, relative to previously proposed methods has high potential for automation and enables to significantly narrow down the field and dynamically track fake reviewers. 



### Data Collection
We scraped data from Amazon's website by adopting snowball method. The process is summarized in the figure below.


Two additional attributes were generated through data aggregation and python module:
- most_rev: highest number of reviews made in a day. This help us to identify if user made a very high number of reviews in the same day. 
- review_sentiment: the sentiment score of the reviews, ranging from -1 (negative) to 1 (positive). This help us identify if the rating is inconsistent with the review sentiment. Textblob module was used to get sentiment score.

#### Overview of final dataset
Total rows: 7652
To download dataset: https://github.com/dindatisi/MSING055_Amazon_Review/
Columns:
- url: Scraped url
- review_bold: Title of the review
- ratings: star rating given by the review
- verified: 1 = reviewer is a verified buyer, 0 = if not
- date: date review was made
- by: name associated with profile 
- profile_id: ID number of profile 
- most_rev: maximum review made in a day by profile
- by_link: url to profile
- helpful: number of people who tagged review as ‘helpful’
- product: product name
- product_link: url to product page
- review_sentiment: sentiment score of the review






