# Amazon_Vine_Analysis


<h1>Project Overview</h1>
Since my work with Jennifer on the SellBy project was so successful, I've been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
In this project, I had access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. I picked one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, I ued PySpark to determine if there is any bias toward favorable reviews from Vine members in your dataset. Then, I wrote a summary of the analysis for Jennifer to submit to the SellBy stakeholders.  

<h1>Resources</h1>

- Data Sources: Amazon_Reviews_ETL_starter_code, challenge_schema.sql

- Software: Google Colab, pgAdmin

- Dependencies: PySpark
<body>
<h1>Summary</h1>

<h3> Amazon Product Reviews</h3>
<p>Using my knowledge of the cloud ETL process, I created an AWS RDS database with tables in pgAdmin, picked a dataset from the Amazon Review datasets, and extracted the dataset into a DataFrame. I transformed the DataFrame into four separate DataFrames that matched the table schema in pgAdmin. Then, I uploaded the transformed data into the appropriate tables and run queries in pgAdmin to confirm that the data has been uploaded.</p>

I selected to work with US Book reviews (https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz)

  
<h3>Determine Bias of Vine Reviews</h3>
  
<p>Using my knowledge of PySpark I determined if there was any bias towards reviews that were written as part of the Vine program. For this analysis, I determined if having a paid Vine review makes a difference in the percentage of 5-star reviews.</p>

Here we can see a DataFrame showing the total number of reviews linked to the Vine program:
  
<img src="https://github.com/kellynichols99/Amazon_Vine_Analysis/blob/main/DataFrame%20of%20Vine%20reviews.png">
  
Next we can see specific numbers:
  
<img src="https://github.com/kellynichols99/Amazon_Vine_Analysis/blob/main/Total%20number%20of%20Vine%20Reviews.png">
  
<img src="https://github.com/kellynichols99/Amazon_Vine_Analysis/blob/main/Vine%20reviews%20with%20five%20stars.png">
  
<img src="https://github.com/kellynichols99/Amazon_Vine_Analysis/blob/main/Percent%20%20of%20Vine%20reviews%20with%20five%20stars.png">
  
Finally we can see a break down of all of the reviews for Amazon Reviews US Books:
  
<img src="https://github.com/kellynichols99/Amazon_Vine_Analysis/blob/main/Determine%20Bias%20of%20Vine%20Reviews.png">
  
<h1>Challange Summary</h1>
As you can see if the file Amazon_Reviews_ETL.ipynb I was able to use ETL to work through the large data set and load that data into multiple tools, such as pgAdmin and Google Colab. Finally I was able to determine that the Vine progame does not appear to be wokring with book reviews and Amazon. I found zero reviews from the Vine program and there for was able to determine that there is not a bias created by Vine reviews. 
  
  I can now easly take this code and skills to review additonal Amazon Review datasets and determine if they show evidance of a bias. This could also show an area of opertunity for the Vine program. With a total of 403807 reviews in this dataset, the Vine program could be beificail for both Amazon and its customers. 
