# Amazon_Vine_Analysis

### An analysis of Amazon's Vine program reviews

## Overview

The purpose of this analysis was to select a dataset from Amazon reviews and extract the data into sql tables (based on review id's, products, customers, and vine reviews). The review data was then filtered to highlight the difference between Vine (paid) and non-Vine (unpaid) reviews. For this analysis, a dataset of video game reviews was used (https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz).

## Results

- The following is a dataframe created using pyspark showing Vine (paid) reviews filtered to include reviews with at least 20 total votes, and at least 50% helpful votes:

![image](https://user-images.githubusercontent.com/79061124/126073956-f1e9d4f3-af3f-40c8-8b2a-05078d054296.png)

- The following is a dataframe created using pyspark showing non-Vine (unpaid) reviews filtered to include reviews with at least 20 total votes, and at least 50% helpful votes:

![image](https://user-images.githubusercontent.com/79061124/126074051-8e1dae9b-51ba-48a9-ae11-ee446f6c2e58.png)

- There were 94 Vine and 40471 non-Vine reviews that met the required criteria (least 20 total votes and at least 50% helpful votes)
- Of the totals that met the required criteria, there were 48 5-star Vine reviews and 15663 5-star non-Vine reviews
- 51.06% of Vine reviews were 5 star and 38.70% of non-Vine reviews were 5 star

## Summary

- The results demonstrate a positivity bias for reviews in the Vine program, based on higher percentage of 5 star reviews (51.06% vs 38.70% for non-Vine)
- It is unclear if this is solely a result of the Vine program, as the sample size of Vine reviews that met the criteria required was far lower than that of non-Vine (94 Vine reviews vs 40471 non-Vine reviews) 
