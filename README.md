# Amazon_Vine_Analysis

## Project Overview

The purpose of this project is to analyze Amazon Vine reviews of products by SellBy. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

From the Amazon Vine website:
> <em>Amazon Vine invites the most trusted reviewers on Amazon to post opinions about products to help their fellow customers make informed purchase decisions. Amazon invites customers to become Vine Voices based on the insightful reviews they published on their past purchases and helpfulness of their reviews. Amazon offers Vine members free products that have been submitted to the program by participating selling partners. Vine reviews are the independent opinions of the Vine Voices and the selling partners cannot influence, modify or edit the reviews. Amazon does not modify or edit Vine reviews, as long as they comply with our posting guidelines.</em>

### Background

This project has outgrown Excel, SQL, and other databases I have used before. This means that I needed to explore the technologies that support the big data ecosystem. In this project, I had access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. I needed to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. The data set I used can be found here: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Wireless_v1_00.tsv.gz. Next, I used PySpark and SQL to determine if there is any bias toward favorable reviews from Vine members in my dataset.

The dataset I used:
![df](https://github.com/JovanHumphrey/Amazon_Vine_Analysis/blob/main/Images/deliverable1_2.JPG)

### Project Results

#### Dataframe Results

![ratings total](https://github.com/JovanHumphrey/Amazon_Vine_Analysis/blob/main/Images/deliverable2_5.JPG)
![paid vines](https://github.com/JovanHumphrey/Amazon_Vine_Analysis/blob/main/Images/deliverable2_3.JPG)
![unpaid vines](https://github.com/JovanHumphrey/Amazon_Vine_Analysis/blob/main/Images/deliverable2_4.JPG)

Below are the questions my analysis aimed to answer:

<p><b>How many Vine reviews and non-Vine reviews were there?</b></p>

This dataset contained 65,547 reviews. Less than 1% of the reviews were by Vine members.

<p><b>How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?</b></p>

Vine members gave 222 out of 613 reviews a 5 star rating.
Non-Vine members gave 30,530 out of 64,934 reviews a 5 star rating.

<p><b>What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?</b></p>

36% of the reviews for Vine members were rated 5 stars.
47% of the reviews for Non-Vine members were rated 5 stars.

### Project Summary

Based on these results we can surmise that paid Vine membership did not influence product reviews. However, while this analysis tells us about Vine reviews for SellBy's wireless products there are 49 other categories to analyze. It may be beneficial to analyze additional datasets before making a unilateral conclusion about all SellBy's products.
