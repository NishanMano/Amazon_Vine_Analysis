# Analysis of Amazon Reviews 

## Overview: 
### About the Amazon Vine Program:
The Amazon Vine Program provides an incentive for a few of their most loyal and trusted reviewers to provide their opinion on a variety of products. There almost are 40+ variety of products such as wireless, watches, office products, home improvement, automotive, etc. Amazon uses a ranking system to select the trusted reviewer based on the quality of the review and how helpful their review was for the other customers. Vendors provide free products to Amazon upon the release of new items. These items are given to the incentivized reviewers, and they would provide their reviews on this product which helps other customers read these reviews on these new items early on.  To avoid conflict of interest, the reviewers are not paid to participate or write favorable reviews. We take this opportunity to use large data in order to arrive at a conclusion regarding any potential biases between these incentivized reviewers. We could also do numerous other analyses with the same dataset using the same concept derived below. 

### Technical Aspect:
AWS (Amazon Web Services) is the world's most comprehensive and broadly adopted cloud platform. I used AWS's relational database to connect with PgAdmin. I then imported the data from S3 (Amazon Simple Storage Service) and connected it to Google Colab Notebook. We use the ETL process on the dataset by using the tool PySpark. PySpark is an open source, distributed computing framework and set of libraries for real-time, large-scale data processing, which would work perfectly with the very large dataset retrieved from Amazon. 

-----
### Dataframe from Google Collab vs. PgAdmin:

Different ways of retrieving the same results using two different methods. I believe that the Google Colab data framework is not as cleanly set up as it is in PgAdmin. In my opinion easier to create data frameworks and get these numbers on PgAdmin in a neater format, however, Google Colab is still very interactive and interesting to use overall. 

### Google Colab:
![Collab](https://i.ibb.co/xq1LsN8/Review-on-Google-Colab.png)

### PgAdmin:
![PgAdmin](https://i.ibb.co/VVMB2FX/Vine-Summary-Paid-vs-Unpaid.png)

------
## Calculations: 
### Percentage of Total Reviews: 
- The total reviews of the incentivized reviewers would equate to approximately 94/40565 = 0.0023 x 100 = 0.23%

- The total reviews of all other reviewers would equate to approximately 40471/40565 = 0.9977 x 100 = 99.77%

### Percentage of Five-Star Reviews:
- Incentivized reviewers equate to approximately 48/15711 = 0.0031 x 100 = 0.31%

- All the other reviewers equate to approximately 15663/15711 = 0.9969% = 99.69%

### Percentage of Five Star Reviews Categorized to Respective Reviewer Groups:
- Incentivized reviewers equate to approximately 48/94 = 0.5106 x 100 = 51.06% 

- All the other reviewers equate to approximately 15663/40471 = 0.3870 = 38.70% 
------
## Results:
I would conclude that there is some sort of positive bias between the incentivized reviewers versus the rest of the reviewers. I strongly believe in the video game database that the incentivized reviewers are providing 5-star reviewers far more than all other reviewers. There can be many possible reasons for this to occur. A good reason in my belief is that these incentivized reviewers can obtain a copy of the game far earlier than others. When video games are released there tends to be a lot of hype around that specific game. Also in certain games, you start seeing more bugs/glitches in games over time that require fixes. Another possibility is that over time people can hack the game, which would attribute to a negative gaming experience for others. I would like to test the other star ratings as this could provide more insight and trends that we may not particularly see only in 5-star reviews.
