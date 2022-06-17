# Amazon_Vine_Analysis

## Project Overview

The purpose of this analysis was to analyze Amazon reviews written by members of the paid Amazon Vine program. An Amazon grocery review dataset was chosen, and PySpark was utilized to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the data into pgAdmin. Finally, PySpark was used to determine if there is any bias toward favorable reviews from Vine members in the chosen dataset.

## Results

Dataframes were created and filtered in order to summarize paid and unpaid vine reviews.


!["Paid Vine Reviews Dataframe"](images/Paid_df.png)


!["Unpaid Vine Reviews Dataframe"](images/Unpaid_df.png)

How many Vine reviews and non-Vine reviews were there? 
 - There were 61 Vine reviews and 28,278 non-Vine reviews for this dataset

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
 - There were 20 paid 5-star vine reviews, and 15,686 unpaid 5-star vine reviews. 
 
What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
 - 32.7% of paid vine reviews were 5-stars, while 55.4% of unpaid vine reviews were 5-stars.


!["Paid Vine Reviews Summary"](images/Paid.png)


!["Unpaid Vine Reviews Summary"](images/Unpaid.png)


## Summary

There doesn't appear to be positivity bias for reviews in the vine program for the current dataset, with about 33% of paid vine reviews being 5-star and around 55% of unpaid vine reviews being 5-star. However, it's difficult to assess bias with such a small number of vine reviews. Had the paid vine review percentage been higher than the unpaid percentage, there would be more of an indication of bias; or if there were more reviews, it would have been a more accurate picture of potential bias.

One additional analysis could be to filter out a smaller number of reviews so there would be a larger total to assess for bias. Or, compiling reviews from multiple datasets in order to use a larger sample size could yield a more valid analysis of bias.
