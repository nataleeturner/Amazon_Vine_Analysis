# Amazon_Vine_Analysis

## Purpose

The purpose of this analysis is to determine whether the Amazon reviews for a US beauty product receive a percentage of 5-star ratings when it is reviewed through the Amazon Vine Program compared to non-Vine reviews. 

## Results

The total number of reviews provided by amazon were first narrowed down to the most relevant and helpful reviews. In order to do this, all reviews that did not have at least 20 helpful votes and the percentage of helpful votes to total votes weren't greater than 50% were eliminated. After this elimination we were still left with 74,760 total votes for this analysis. The dataframe with the narrowed down results is seen below.

<img width="663" alt="helpful_vine_df" src="https://user-images.githubusercontent.com/88349443/145734089-37497479-5b43-4e01-87b4-a4218565c268.png">

These reviews were then analyzed and the following results were realized:

* Out of the 74,760 total votes, 647 of these were paid for through the Amazon Vine program and the rest, 74,113 were not. This was determined by filtering the data for reviews that had a "Y" or "N" in the vine column, as seen in the following two data frames.

<img width="665" alt="helpful_vine_yes" src="https://user-images.githubusercontent.com/88349443/145734101-2d9871d9-d989-4aa5-80e9-7866dc1e7f0e.png">
<img width="661" alt="helpful_vine_no" src="https://user-images.githubusercontent.com/88349443/145734104-67639036-f6e2-43b6-8f82-e239ef7612be.png">

* Of the 647 Vine reviews, 229 of them were 5 stars. Of the 74,113 unpaid reviews, 43,217 of them were five stars. This was done by counting the number of rows in the previous data frames had a "5" in the "star_rating" column.

* Dividing the 5 star reviews by total reviews for each paid and unpaid, we can see that 35.4% of the Vine reviews received five stars and 58.3% of the non-Vine reviews received 5 stars.


## Summary

Based on these results, there is no perceived positivity bias in the Vine reviews vs the non-Vine reviews. In fact, there is a much higher percentage of five star reviews that were not through the Vine program than those that did come in through the Vine program. In order to validate this data, I would recommend taking into account whether the purchase was verified or not. At first glance, it looks like the percentage of reviews that were also verified purchases is higher in the non-Vine reviews than in the Vine reviews. If there is a large discrepancy in the amount of people reviewing the product that never actually purchased or used the product then removing the non-verified purchase reviews could greatly alter the results of this analysis. Lastly, using the average star rating of all the vine vs non-vine reviews instead of just the total five star reviews would be an interesting analysis. It's possible that the number of 4 and maybe even 3 star reviews could affect the average and, therefore, our results.
