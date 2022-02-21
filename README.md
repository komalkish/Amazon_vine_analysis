# Amazon_vine_analysis

# Overview of the Analysis
The analysis focuses on Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. For this project, I accessed approx.fifty reveiw datasets of Amazon and each one contains reviews of a specific product, from clothing apparel to wireless products. 

## Selection of Review Category
Pet Products - https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Pet_Products_v1_00.tsv.gz
# Purpose
I picked pet products as my category to perform analysis and utilized PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I used PySpark to determine if there is any bias toward favorable reviews from Vine members in the dataset.

# Summary 
## Step 1 - Perform ETL on Amazon Product Reviews
Using the knowledge of the cloud ETL process, I created an AWS RDS database with tables in pgAdmin, picked a dataset from the Amazon Review datasets (see above, selection of review category), and extracted the dataset into a DataFrame. Further, I transformed the DataFrame into four separate DataFrames that match the table schema in pgAdmin. Then, I uploaded the transformed data into the appropriate tables and run queries in pgAdmin to confirm that the data has been uploaded.
<img width="1093" alt="image" src="https://user-images.githubusercontent.com/92557075/154871671-f205e4f5-29c8-46a6-b2cf-62e7d3f57490.png">

<img width="1114" alt="image" src="https://user-images.githubusercontent.com/92557075/154871691-82c6fe6c-6614-4b47-a95a-2aeef261d687.png">

## Step 2 - Determine Bias of Vine Reviews
Using PySpark, I determined if there is any bias towards reviews that were written as part of the Vine program. For this analysis, I analyzed if having a paid Vine review makes a difference in the percentage of 5-star reviews.
# Results 
1. Total 5 star rating for both, Vine and Non Vine program = 35730
2. Total Vine reviews = 63
3. Total Non Vine reviews = 19437
4. Vine star Rating percentage = 17%
5. Non Vine start rating percentage = 54%
* Per the analysis, paid vine review does not make a difference in the percentage of 5- Star rating.
<img width="1014" alt="image" src="https://user-images.githubusercontent.com/92557075/154872541-ddbbb11f-5c25-4efc-b42e-4b1a7b737708.png">
Recomendation
To further analyze for all rating below 5. 
