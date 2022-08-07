# Amazon Vine Analysis

## Overview

Our task for this project is to analyze Amazon reviews written by members of the paid Amazon Vine Program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

With access to approximately 50 datasets, each containing reviews of a specific product, we will be choosing one of the datasets to perform an analysis on. Specifically, we have chosen to look at camera reviews. Using Pyspark, we analyze the dataset by:
* Performing the ETL process to extract the dataset
* Transforming the data
* Connecting to an AWS RDS instance
* Loading the transformed data into pgAdmin

Then, we will further our analysis with PySpark to determine if there is any bias toward favorable reviews from Vine members in our dataset. Below is the summary of our results.

## Results

### I. Vine reviews vs non-Vine reviews

From our analysis, the total number of reviews was 51,123.

<img width="303" alt="Screen Shot 2022-08-07 at 11 35 35 AM" src="https://user-images.githubusercontent.com/101564349/183298826-77fd89f4-ba3d-4b6a-b853-02f1989d08d1.png">

Of those 51,123 reviews, there were a total of 607 paid reviews and 50,516 unpaid reviews. 

<img width="400" alt="Screen Shot 2022-08-07 at 11 36 35 AM" src="https://user-images.githubusercontent.com/101564349/183298846-256ca21c-2f08-4d58-a3ff-ae8e329fdee1.png">

### II. 5-star Vine reviews vs 5-star non-Vine reviews

From our analysis, we gathered that the total number of 5-star reviews were 25,473. 

<img width="461" alt="Screen Shot 2022-08-07 at 11 38 54 AM" src="https://user-images.githubusercontent.com/101564349/183298949-143038c5-0b9d-4b4d-8979-28617190ade5.png">

Of those 25,473 5-star reviews, 257 were paid while 25,300 were unpaid reviews.

<img width="462" alt="Screen Shot 2022-08-07 at 11 39 47 AM" src="https://user-images.githubusercontent.com/101564349/183298996-92359faf-4a09-4aa8-8a1f-6098d2096c01.png">

### III. Percentage of 5-star Vine reviews vs percentage of 5-star non-Vine reviews

Lastly, we determined the percentage of 5-star Vine reviews and the percentage of 5-star non-Vine reviews. From the image below, we can conclude that the majority of 5-star reviews belonged to non-Vine reviews, with a approximately 99%. The percentage of 5-star Vine reviews fell behind at roughly 1%.

<img width="432" alt="Screen Shot 2022-08-07 at 11 41 14 AM" src="https://user-images.githubusercontent.com/101564349/183299069-db9dcdba-daec-4c8c-aac5-9d53bfa5fb0d.png">

## Summary

From our analysis, it does not appear that there is a strong bias toward 5-star reviews from paid Amazon Vine reviewers. Conversely, it appears that Vine reviews may be a bit more critical. Out of 607 Vine reviews, there were only 257 that were 5-star which makes up approximately 42% of all Vine reviews. On the other hand, out of 50,516 non-Vine reviews, there were a total of 25,300 5-star reviews, making up approximately 50% of all non-Vine reviews. An additional analysis that could be conducted on our dataset is the relationship between 4-star reviews on Vine reviews versus non-Vine reviews. 
