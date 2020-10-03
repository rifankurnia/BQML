# BQML
Machine Learning using BigQuery


Dataset

Google Analytics sample dataset for BigQuery
The sample dataset provides an obfuscated Google Analytics 360 dataset that can be accessed via BigQuery. It’s a great way to look at business data and experiment and learn the benefits of analyzing Google Analytics 360 data in BigQuery.



To access the dataset:

Go to http://bigquery.cloud.google.com.

If you're new to BigQuery (or you don't have a project set up yet) you need to create a project.

Once you have a project, use this link to access the dataset.

Click Query Table to run a query.

In the future you can access the dataset within BigQuery by selecting the bigquery-public-data project from the left-hand navigation panel, then select the ga_sessions table under the google_analytics_sample dataset.

Where it comes from
The sample dataset contains obfuscated Google Analytics 360 data from the Google Merchandise Store, a real ecommerce store. The Google Merchandise Store sells Google branded merchandise. The data is typical of what you would see for an ecommerce website. It includes the following kinds of information:

Traffic source data: information about where website visitors originate. This includes data about organic traffic, paid search traffic, display traffic, etc.
Content data: information about the behavior of users on the site. This includes the URLs of pages that visitors look at, how they interact with content, etc.
Transactional data: information about the transactions that occur on the Google Merchandise Store website.
Ways to use it
Because it provides Google Analytics 360 data from an ecommerce website, the dataset is useful for exploring the benefits of exporting Google Analytics 360 data into BigQuery via the integration. Once you have access to the dataset you can run queries such as those in this guide for the period of 1-Aug-2016 to 1-Aug-2017. For example to see the total pageviews the website received for 1-Jan-2017 you would query the dataset with:

SELECT SUM(totals.pageviews) as TotalPageviews

FROM [bigquery-public-data:google_analytics_sample.ga_sessions_20170101]

Limitations
All users have viewer access to the dataset. This means that you can query the dataset and generate reports but you cannot complete administrative tasks. Data for some fields have been obfuscated such as fullVisitorId, or removed such as clientId, adWordsClickInfo and geoNetwork. “Not available in demo dataset” will be the returned for STRING values and “null” will be returned for INTEGER values, when querying the fields that contain no data.
