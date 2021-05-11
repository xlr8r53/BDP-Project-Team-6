
#                                               CSEE 5590/490: BIG DATA PROGRAMMING - FINAL REPORT

**Instructor : Zeenat Tariq**

**Team Number : 6**

## PROJECT TITLE AND TEAM MEMBERS

### International Student Data Analysis using Big Data.

- Tanvi Jain

- Saikumar Reddy Papagari

- Amarnadha Reddy Ankireddypalli

- Thotakura Naga Mounika


##  INTRODUCTION 

This project focuses on extraction of dataset (Twitter Data) from the Twitter API regarding all the information related to international students and using different tools like Hive, Hue, Scala, pySpark, Spark SQL and Solr to show different aspects of the data in a visualization form using Tableau and Seaborn.

GitHub Link: https://github.com/xlr8r53/BDP-Project-Team-6/wiki/Final-Report-Submission

PPT Link: https://github.com/xlr8r53/BDP-Project-Team-6/blob/fe992332219ce41cb6877a771786d0d9fb77d02e/Final_Presentation.pptx

Video Link: https://umkc.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=1367520c-3de7-4ecb-825f-ad25001fd55c

## BACKGROUND

Twitter sentiment analysis is done in different ways before, using panda is the most common way. We will be using different hashtags which are related to international students and events related to international students to get a hold of better results based on those hashtags and more information about what events really took place and different aspects they bring out. Here are some references of projects people have done implementing twitter analysis with big data, we are going to follow some aspects of these projects, but our dataset is new and is extracted only for this project, so we could only find references related to those projects which have totally different dataset and completely different objectives. 

- https://github.com/dsuarez993/bigdata-realtime-twitter-analysis

- https://github.com/6vedant/TwitterAnalyticsHadoop

- https://www.toptal.com/apache/apache-spark-streaming-twitter


## GOALS AND OBJECTIVES

### Motivation:

Studying abroad is a journey of education and discovery. There are currently over 1 million international students from more than 220 countries, coming to the United States annually. The individuals from this group belong to the international student community and we came to the United States to get a higher education. There are numerous situations where we are relied upon to follow those standards which the overall US citizens are not expected to follow in the long run since we have a place with the foreigner gathering. So, this gave us the establishment for this task, and we chose to feature the fundamental information like percentage of students going to the United States for education, the probability of getting a work VISA, Immigration rules change for F-1 Visa during COVID, Jobs for international students during Covid (H1B sponsorship).

### Significance:

Big data tools help to analyze the huge data which helps to provide efficient results. The sentimental analysis provides a brief understanding of various challenges that international students are currently facing and impact of covid-19 on the visa assurance. Finally, we are using Spark using python and Scala for writing the queries by visualizing with Seaborn and Tableau. 

### Objectives:
The objective of this project is to get twitter data extraction using Twitter Data Analysis and then cleaning the data, performing sentiment analysis, and importing files into Hadoop where we used different tools like Hue, Hive, Solr, Scala, Spark SQL and pySpark.

### Features:

The main feature of the project is to collect the Real timed tweets from the twitter API, also by performing the ETL which means we preprocess the data using Texthero and extract the necessary data and then we load the extracted data in our HIVE. Performed topic modelling using LDA and genism model, visualized the top 4 topics by t-SNE visualization and performed analysis on data using PySpark, Solr and Scala

## DATASET:

We collected the data using twitter API using developer account and API keys. We have used different hashtags to get data related to 3 different scenarios as follows: 

1. Generic International Student Data (#F1visa, #intlstudents, #internationalstudents, #studyinUSA) 

2. Immigration rules change for F1 Visa during COVID in 2020 (#AbolishICE) 

3. Jobs for international students during covid (H1B sponsorship) (#H1B, #h1bjobs) From the extraction we have the information about the tweet itself like this:

The information about the user as well - It has all the different fields, which we will filter and use later using big data tools to perform queries and visualization.

It has all the different fields, which we will filter and use later using big data tools to perform queries and visualization. 
Features and their description:  

![image](https://user-images.githubusercontent.com/78001524/117752496-7ba0f680-b1dc-11eb-9b3c-62c14978b405.png)

			Table: Description of Attributes of Data


### Detail design of Features with Project Workflow:

![image](https://user-images.githubusercontent.com/78001524/117752342-354b9780-b1dc-11eb-9b44-b100dbb79354.png)


## DATA ANALYSIS:

We have extracted dataset using twitter API, these datasets are extracted using different hashtags focusing on different events related to international students, dividing the events and dataset is crucial since we want this project to be informational and focus on different aspects through different datasets. We will use sentiment analysis on the text (tweet) and use different queries to extract important features and visualize them in Tableau. 
Data Collection:

![image](https://user-images.githubusercontent.com/78001524/117752544-95dad480-b1dc-11eb-97c9-8072ac64d9e7.png)


### Data Preprocessing:


a.
![image](https://user-images.githubusercontent.com/78001524/117752561-9d01e280-b1dc-11eb-962f-8d9363f3110a.png)


b.
![image](https://user-images.githubusercontent.com/78001524/117752571-a1c69680-b1dc-11eb-9924-a32f4a187ae7.png)

Fig. Plotting the Top words from the data.

c.
![image](https://user-images.githubusercontent.com/78001524/117752582-a7bc7780-b1dc-11eb-8b97-21482d8f49f6.png)
	
Fig: Adding PCA and k-means clusters to the preprocessed data.

d.
![image](https://user-images.githubusercontent.com/78001524/117752591-ab4ffe80-b1dc-11eb-8618-74957062e444.png)

Fig: Scatter plot hovering the k-means and PCA clustered data


## IMPLEMENTATION:




## **Solr:**

**1. Creation/generation of instance & Collection:**

![image](https://user-images.githubusercontent.com/78001524/112710684-1b0a6400-8e91-11eb-9aa8-3594fd26250a.png)


**2. Edit the schema.xml created with the instance generation inside the configuration folder to change
the attributes based on the dataset given:**

![image](https://user-images.githubusercontent.com/78001524/112710693-21004500-8e91-11eb-9957-7a65eed380ca.png)


**3. Open the solr browser in the web browser and select the create collection on the left side
dropdown.**

![image](https://user-images.githubusercontent.com/78001524/112710699-252c6280-8e91-11eb-8560-5eba43aa0048.png)


**4. Set "Tweet Id" as the primary key.**

![image](https://user-images.githubusercontent.com/78001524/112710700-29f11680-8e91-11eb-9c6f-0ff30ce95152.png)


**5. Select the document type to csv. Then copy paste all the data inside the dataset into the
documents field and submit the document.**

![image](https://user-images.githubusercontent.com/78001524/112710702-2e1d3400-8e91-11eb-9310-849805c069e9.png)

## **Queries**

**1. Pulled the 10 records of data:**

![image](https://user-images.githubusercontent.com/78001524/116711911-ececd800-a998-11eb-88f3-ea1939d6a42f.png)

**2. Pulled the tweets that are tweeted in English:**

![image](https://user-images.githubusercontent.com/78001524/116645554-b896fe80-a93b-11eb-9cf3-677c7426937b.png)

**3. Pulled the data has 'F1Visa' included in the Text (Regex):**

![image](https://user-images.githubusercontent.com/78001524/116711344-5fa98380-a998-11eb-83db-2efb4ee0b0be.png)

**4. Collected the response with having Text:”student” and Text:”USA”:**

![image](https://user-images.githubusercontent.com/78001524/116838611-94822a00-ab94-11eb-9ba2-3615b1c7616c.png)

**5. Pulled the most retweeted tweets:**

![image](https://user-images.githubusercontent.com/78001524/116842440-33f9e980-aba2-11eb-888f-15d839ebdf26.png)


**Converting working dataset (in .csv) to .json file.** 

![image](https://user-images.githubusercontent.com/78001524/117752706-e05c5100-b1dc-11eb-9ce4-fd206a4894d2.png)


**Place the .json file in the cloudera working directory.**

![image](https://user-images.githubusercontent.com/78001524/117752713-e4886e80-b1dc-11eb-89d4-647437e32f01.png)


## Spark using Scala


**1. Starting the scala using spark-shell command.**

![image](https://user-images.githubusercontent.com/78001524/117360257-2bddca80-ae7e-11eb-87f5-9768655ebab6.png)

**2. Load the 'dat1.json' into a  data frame using sqlContext.read.json()**

![image](https://user-images.githubusercontent.com/78001524/117360378-562f8800-ae7e-11eb-89f6-f6fd366c76b1.png)

**3. Schema of the dataset.**

![image](https://user-images.githubusercontent.com/78001524/117360818-d9e97480-ae7e-11eb-88c3-eb3c7d3b6a44.png)

**4. Display the Username and Text of top 20 tweets.**

![image](https://user-images.githubusercontent.com/78001524/117361618-e15d4d80-ae7f-11eb-88db-74f5a08afe17.png)

**5. Count the number of Media Types present in the dataset.**

![image](https://user-images.githubusercontent.com/78001524/117365899-9e05dd80-ae85-11eb-809e-1f1b79365487.png)

**6. Fetching the different languages in which the tweets are made about international students.**

![image](https://user-images.githubusercontent.com/78004048/117381384-918f7e00-aea1-11eb-99c4-4efface7a84f.png)

**7. Fetching users with a greater number of hashtags in their tweets on student data.**

![image](https://user-images.githubusercontent.com/78004048/117386048-cf919f80-aeab-11eb-8527-f4cd7a0e9311.png)

**8. Fetching users who have more followers and are tweeting based on student data.**

![image](https://user-images.githubusercontent.com/78004048/117383124-a110c600-aea5-11eb-8d15-641763382fbc.png)

**9. Fetching users with a greater number of mentions in their tweets on student data.**

![image](https://user-images.githubusercontent.com/78004048/117386084-de785200-aeab-11eb-892a-5cc10a8ed1ab.png)

**10. Fetching users having account names with a greater number of tweets on web series.**

![image](https://user-images.githubusercontent.com/78004048/117385130-0ff01e00-aeaa-11eb-9ec2-2828a5591f42.png)

**11. Fetching users with a greater number of retweets for their tweets on student data**.

![image](https://user-images.githubusercontent.com/78004048/117385526-eedbfd00-aeaa-11eb-8e43-9a4a437b05e9.png)

## Spark using Python

Considered python programming because it is much quicker than Scala data-frames in terms of execution time – Visualization is achieved with Matplotlib and Seaborn in python programming.


1. Download Java to run the Java Virtual Machine (JVM).

![image](https://user-images.githubusercontent.com/78001524/113907937-93c7c500-979b-11eb-9b5f-e014f07abe93.png)

2. Set the environment path. This will enable us to run Pyspark in the Colab environment.

![image](https://user-images.githubusercontent.com/78001524/113908021-af32d000-979b-11eb-8053-2558bd7e6bd9.png)


3. Import SparkSession from pyspark.sql and create a SparkSession.

![image](https://user-images.githubusercontent.com/78001524/117051164-d8cc1200-acdb-11eb-954b-f9f1fa99e593.png)

![image](https://user-images.githubusercontent.com/78001524/117051366-14ff7280-acdc-11eb-8e06-3d28c0cd16f6.png)


**1. Import the dataset and create data frames directly on import.**

![image](https://user-images.githubusercontent.com/78001524/117051913-acfd5c00-acdc-11eb-9f0e-a35c1da547be.png)

**2. Check for duplicate records and null values in the dataset.**

![image](https://user-images.githubusercontent.com/78001524/117052170-05345e00-acdd-11eb-957e-8a4200bf84f2.png)

## Queries:

**1. Display first 100 rows order by the Date tweeted.**

![image](https://user-images.githubusercontent.com/78001524/117173309-40dd2f80-ad92-11eb-960a-9e423448a69b.png)

**2. Count the  number of tweets based on the sources of data by performing the Union operation.**

![image](https://user-images.githubusercontent.com/78001524/117173597-8ac61580-ad92-11eb-9869-3612e89b900b.png)

![image](https://user-images.githubusercontent.com/78001524/117173727-acbf9800-ad92-11eb-88b5-4d36606fdcbb.png)

**3. Counted the tweets by grouping into languages and order in descending order with pulling top 5.**

![image](https://user-images.githubusercontent.com/78001524/117174097-fe682280-ad92-11eb-9f34-6779dc2cca02.png)

![image](https://user-images.githubusercontent.com/78001524/117174135-0758f400-ad93-11eb-8b22-16d4cfffc6f2.png)

**4. Pull the top 10 user_name by followers_count by dropping the duplicates.**

![image](https://user-images.githubusercontent.com/78001524/117174555-733b5c80-ad93-11eb-8643-e333c2c4fe9a.png)

![image](https://user-images.githubusercontent.com/78001524/117174373-4129fa80-ad93-11eb-906d-b79cb9791543.png)

**5. Pull the count of tweets based on the desired topics from the Text attribute.**

![image](https://user-images.githubusercontent.com/78001524/117174728-a54cbe80-ad93-11eb-9db6-f4d2fc1ff944.png)

![image](https://user-images.githubusercontent.com/78001524/117174775-b09fea00-ad93-11eb-8b10-1bdc97b5e6f5.png)

**6. Display the screen names of tweets that are mostly retweeted.**

![image](https://user-images.githubusercontent.com/78001524/117175447-7aaf3580-ad94-11eb-97fc-064706715248.png)

![image](https://user-images.githubusercontent.com/78001524/117175469-83077080-ad94-11eb-9410-154ea7709df7.png)

**7. Display the screen name of tweets that has highest mentions.**

![image](https://user-images.githubusercontent.com/78001524/117175551-99153100-ad94-11eb-8934-84783cfdab39.png)

![image](https://user-images.githubusercontent.com/78001524/117175876-e6919e00-ad94-11eb-9689-a34a042f70cc.png)

**8. Display the screen name of tweets that has most hashtags in it.**

![image](https://user-images.githubusercontent.com/78001524/117176943-10979000-ad96-11eb-9f11-45bb0c6b5f7f.png)

![image](https://user-images.githubusercontent.com/78001524/117177057-358c0300-ad96-11eb-8db0-b67c5588964e.png)

**9. Plot the Users with highest number of MediaURLs.**

![image](https://user-images.githubusercontent.com/78001524/117178631-dfb85a80-ad97-11eb-85b6-90988dec3032.png)

![image](https://user-images.githubusercontent.com/78001524/117178773-01b1dd00-ad98-11eb-9171-e2d1ba98cfb8.png)

**10. Display the count of different types of tweets (Retweet, Reply or Tweet).**

![image](https://user-images.githubusercontent.com/78001524/117179961-50ac4200-ad99-11eb-9597-63e22cd868a5.png)

![image](https://user-images.githubusercontent.com/78001524/117180198-8d783900-ad99-11eb-86c3-e98e32a43d9a.png)


**11. Analysing the user data with pyspark:**

![image](https://user-images.githubusercontent.com/78001524/117753280-d2f39680-b1dd-11eb-947c-0bdb09a57d3e.png)

**12. Checking the number of verified and unverified accounts tweeted about the international student cause.**

![image](https://user-images.githubusercontent.com/78001524/117753329-e4d53980-b1dd-11eb-8280-79e5b7f2a24f.png)

**13. From this visualization it shows that there were more tweets in the year 2020 specifically as compared to other years since international students were in the talk in this year due to the corona pandemic, when ICE decided to change the immigration rules and h1b sponsorship was affected due to lack of jobs and recession.**

![image](https://user-images.githubusercontent.com/78001524/117753339-ea328400-b1dd-11eb-918e-fa64bb94dc40.png)

**14. Here are the countries that tweeted most and the least regarding international student scenario in United States specifically.**

![image](https://user-images.githubusercontent.com/78001524/117753347-edc60b00-b1dd-11eb-917c-12589596bf18.png)

**Pyspark, Spark SQL, NLP and SQL queries for both users and tweets:**
 
Here are 2 datasets, one covers the information about the tweets, and other about the users. 

![image](https://user-images.githubusercontent.com/78001524/117753359-f4548280-b1dd-11eb-97c7-8e5c6a7ad8ce.png)

Changing the Spark SQL Dataframe Column type from one data type to another data to make the analysis more accurate and meaningful.

![image](https://user-images.githubusercontent.com/78001524/117753372-fa4a6380-b1dd-11eb-834a-afcd1d0f4b08.png)


**Spark SQL Queries**

![image](https://user-images.githubusercontent.com/78001524/117753397-06cebc00-b1de-11eb-9197-e0194c2cb503.png)

![image](https://user-images.githubusercontent.com/78001524/117753411-0cc49d00-b1de-11eb-8fc6-58b5580b2787.png)

![image](https://user-images.githubusercontent.com/78001524/117753417-10582400-b1de-11eb-90fd-6596bebbc0bc.png)

The total number of verified users who participated in tweeting for the international students, their followers, the people they are following and the favorites. 

![image](https://user-images.githubusercontent.com/78001524/117753428-151cd800-b1de-11eb-8ed2-7fa3adaddba8.png)

**Tweets Data**

![image](https://user-images.githubusercontent.com/78001524/117753442-19e18c00-b1de-11eb-973e-ae0400cd52c3.png)

![image](https://user-images.githubusercontent.com/78001524/117753452-1e0da980-b1de-11eb-856f-bffb2c55f254.png)

![image](https://user-images.githubusercontent.com/78001524/117753466-236af400-b1de-11eb-8d49-f7d0bc6f16f6.png)

Sentiment Analysis Trend with time for the year 2020:- 

![image](https://user-images.githubusercontent.com/78001524/117753482-282fa800-b1de-11eb-9551-fe856c8fc15b.png)

Visualization of the trend of the tweets by verified and non verified users for the different years regarding the international students and ICE immigration rule changes, It also includes the tweets about h1b sponsorship. 

![image](https://user-images.githubusercontent.com/78001524/117753496-2cf45c00-b1de-11eb-9155-ad84cf23731e.png)


## HIVE:

**Created the database and database table in hive and loaded the data into hive table for AbolishICE dataset:**

![image](https://user-images.githubusercontent.com/78001524/117753860-d2a7cb00-b1de-11eb-916f-63023ea5b999.png)
![image](https://user-images.githubusercontent.com/78001524/117753864-d50a2500-b1de-11eb-987a-e36760404a82.png)

**Created the database and database table in hive and loaded the data into hive table for F1visa dataset:**
**Visualized the output:**
 
![image](https://user-images.githubusercontent.com/78001524/117753868-d9364280-b1de-11eb-91a9-ca06930b395a.png)

**Created the database and database table in hive and loaded the data into hive table for h1b dataset:**
**Visualized the output:**

![image](https://user-images.githubusercontent.com/78001524/117753876-dfc4ba00-b1de-11eb-8316-806a41b708ec.png)


**Created the database and database table in hive and loaded the data into hive table for intlstudents dataset:**
**Visualized the output:**

![image](https://user-images.githubusercontent.com/78001524/117753886-e4896e00-b1de-11eb-938f-c50d8490f6ac.png)


**Created the database and database table in hive and loaded the data into hive table for study in USA dataset:**
**Visualized the output:**

![image](https://user-images.githubusercontent.com/78001524/117753893-e8b58b80-b1de-11eb-9855-0e00c3785713.png)


**Imported file into hdfs**

![image](https://user-images.githubusercontent.com/78001524/117753900-ec491280-b1de-11eb-90ae-58d436106f24.png)
![image](https://user-images.githubusercontent.com/78001524/117753906-efdc9980-b1de-11eb-83f2-2784e1cb2a93.png)

**Created the database and database table in hive and loaded the data into hive table for General dataset:**

![image](https://user-images.githubusercontent.com/78001524/117753942-fc60f200-b1de-11eb-9409-68969c160e02.png)
![image](https://user-images.githubusercontent.com/78001524/117753952-ff5be280-b1de-11eb-8319-f31748909e19.png)

**Visualized the Output:**
![image](https://user-images.githubusercontent.com/78001524/117753963-02ef6980-b1df-11eb-8fe3-eaca74514032.png)


### Queries:

**1. Viewing the number of tweets based on h1b:**

![image](https://user-images.githubusercontent.com/78001524/117753967-05ea5a00-b1df-11eb-82bb-3dca0ab9e0dd.png)

**2. Viewing the number of tweets based on F1visa:**

![image](https://user-images.githubusercontent.com/78001524/117753981-0b47a480-b1df-11eb-9a9c-167363397864.png)

**3. Details of tweets regarding international students that have a greater favourites count:**

![image](https://user-images.githubusercontent.com/78001524/117753991-0edb2b80-b1df-11eb-964e-7113144f3128.png)

**4. Details of tweets regarding international students using Order by:**

![image](https://user-images.githubusercontent.com/78001524/117754000-14387600-b1df-11eb-9489-d42e6e5a5bae.png)

**5. Viewing the details of tweet id from h1b:**

![image](https://user-images.githubusercontent.com/78001524/117754003-17cbfd00-b1df-11eb-9713-75c167bb21d8.png)

**6. Details of retweets with limit from h1b:**

![image](https://user-images.githubusercontent.com/78001524/117754013-1bf81a80-b1df-11eb-97d7-0cb80d17865b.png)


## RESULTS EVALUATION:

a.
![image](https://user-images.githubusercontent.com/78001524/117753738-9bd1b500-b1de-11eb-8c23-649d6091ceae.png)


b.
![image](https://user-images.githubusercontent.com/78001524/117753743-9ffdd280-b1de-11eb-8223-913fee39f2f4.png)


c.
![image](https://user-images.githubusercontent.com/78001524/117753753-a429f000-b1de-11eb-82d5-e551dc149010.png)


d.
![image](https://user-images.githubusercontent.com/78001524/117753763-a8560d80-b1de-11eb-8171-4aeae086d133.png)


e.
![image](https://user-images.githubusercontent.com/78001524/117753773-ac822b00-b1de-11eb-9837-3679b19c300f.png)

Fig. Plotting top words from Text data

f.
![image](https://user-images.githubusercontent.com/78001524/117753802-b9068380-b1de-11eb-8887-2dcd4e6e5633.png)

Fig. Word Cloud generation using Texthero

g.
![image](https://user-images.githubusercontent.com/78001524/117753825-bf94fb00-b1de-11eb-9aee-fcdef97508e3.png)

Fig. Scatter Plot of PCA and k-means cluster analysis


## CONCLUSION:

Done the data extraction using Twitter API for different hashtags and implemented them in various Big Data tools like Hive, Spark and PySpark. The visualization is done using PySpark in the form of bar graphs, pie-charts, and scatter plots. The sentiment analysis of the tweets is performed using pyspark and some visualization is done using different tools like TSNE and tableau. 

## FUTURE WORK:

* Implementing the better Machine Learning Algorithms.
* Working on more data sources such as Instagram, Facebook, and YouTube Data as well. 
* Considering  the project deployment in Docker.
* Better use of the big data tools by targeting on a specific predefined  and focused dataset. 
* A tool can be created using ML tools and analysis which on the basis of streaming tweets can tell the sentiments and prospective suggestions about a specific situation or crisis, which would help people calm down and be productive in the right track instead of panicking. 

## PROJECT MANAGEMENT:

**Description:**

All the tasks that were lined up for the final project have been completed successfully in a timely fashion. We were able to implement different big data tools to analyse the data about international students and how they were impacted by the COVID situation and crisis. 

**Work Completed :**

We have completed the extraction of dataset from twitter using twitter API, completed the tweets preprocessing part, sentiment analysis of those tweets. The data which was extracted was converted from csv to json format. We have also worked on Hive, Scala and pySpark to perform different analyzing techniques. Loaded dataset into solr to analyze various aspects from the data. Visualized the results using Tableau and Seaborn.

**Responsibility (Task, Person):**

* Twitter data streaming (Tanvi, Mounika)
* Data processing (Tanvi, Amar)
* Conversion of csv to json (Saikumar)
* Spark streaming using Scala (Saikumar)
* Solr execution and queries (Amar)
* pySpark queries and plotting (Amar, Tanvi)
* Word cloud, PCA and k-means clustering using Texthero (Amar)
* Hive implementation (Mounika)
* Visualization in Seaborn (Amar)
* Word Cloud using pyspark (Tanvi)
* Topic modelling to find dominant terms (Tanvi)
* TSNE clustering & Visualization in Tableau (Tanvi)
* Sentiment analysis and trend analysis in pyspark(Tanvi)

**Contributions (members/percentage):**

* Tanvi Jain (25%)
* Amarnadha Reddy Ankireddypalli (25%)
* Naga Mounika Thotakura (25%)
* Saikumar Reddy Papagari (25%)

## Issues/Concerns:

* The data we gathered from Twitter in the beginning is unprocessed. So, we faced challenges in combining all the extracted .csv files into one single file.
* Faced challenges in converting .csv file to .json file due to large data.

## STORY TELLING:

WHO
WHAT
WHEN
WHERE
WHY
HOW

### CHAPTER 1

1. The international students who are studying in the United States of America (or overseas)

2. The problem mainly affected them in terms of finance, job hunting, allowance to work with any company at any time or lack of getting accepted by any company due to limited work authorization and stress because of lack of stability in life.

3. There is no specific time/place of problem, it is the general situational challenges that international students come across.

4. These challenges can be faced by international students in a foreign land, where they are a part of the immigrant community and do not have access to the perks that the citizens of that country get, which makes life a bit harder for even the very basic requirements of living.

5. Due to a set of immigration rules and less availability of jobs/ work authorization in desired fields.

6. There is not a certain time that the chances of happenings like these because these kinds of incidents are seen and experienced by many international students over the time.

### CHAPTER 2

1. The international students who are studying in the United States of America (or overseas). The dataset is extracted using different hashtags to get data related to 3 different scenarios as follows:

Generic International Student Data (#F1visa #intlstudents #internationalstudents #studyinUSA)
Immigration rules change for F1 Visa during COVID in 2020 (#AbolishICE)
Jobs for international students during covid (H1B sponsorship) (#H1B, #h1bjobs)

2. Yes, the data set records the targeted events, activities, behaviors, etc. in Assignment 1. This is fundamentally about the variables. It records the username, the location, the tweets which tell us about what the users really think about the specific event that happened.

3. The events take place on how people reacted to the challenges faced by International students during COVID such as immigration  rules for F1visa, jobs for international students during covid(H1B sponsorship).

4. These challenges can be faced by any International Student in a foreign land, where they are a part of immigrant community and do not have access to the perks that the citizens of that country get, which makes life a bit harder for even the very basic requirements of living.

5. Due to the increase in the intake of international students over a period.

6. It happened during COVID, as a result there was a massive unavailability of jobs (new graduates), many have lost their jobs due to pandemic, immigration rules change for F1 Visa during COVID.


### CHAPTER 3 (Scientist and AI)

- Students from other countries studying in the United States of America or Overseas

- The preprocessed data can be fitted to any of the ML and Deep Learning models. The text is used for finding dominant topic through topic modeling and sentiment analysis. All the other features of the data about tweet and users are used to visualize the important stats using pyspark. 

- The extracted data can be used to find the accuracy and runtime performance of best fitting ML model. 

- It was part of the Big Data Programming course offered in University of Missouri-Kansas City

- Most of the unsupervised learning models work best for our extracted data.

- The data scientist may use data in the way that the research requires or based on the tool. Nothing in this method is static; new data or data sources may be introduced as required for further review.


### CHAPTER 4 (Users)

- International students  
 
- The visualisation shows the analysis of twitter data on international students through which we analysed various challenges faced by them due to covid.
 
- This project can be used to understand the present crisis due to covid such as travel ban, student’s in-take, and visa issues. 
 
- This project is visualised using Seaborn and Tableau and can be deployed in Docker as well.
 
- The visualised data can be used to comprehend the travel bans, college admissions, and visa issues due to covid crisis.

- The international students can utilize this project work to plan their overseas study in a better way  considering all the challenges that may face by them oncourse of their overseas journey.


### CHAPTER 5 (Society)

- In this project the society of international students/immigrants in the USA are targeted during the covid crisis. The data scientists who have worked on this project are a part of the international student society who thought it was necessary to address this situation and analyse it through using big data tools. Data Scientists - Tanvi Jain, Saikumar Reddy Papagari, Amarnadha Reddy Ankireddypalli, Thotakura Naga Mounika. 
 
- Yes definitely there is a social and cultural impact through this project, since it will help to identify how people were effected and there was a drastic change in the nature of tweets for this situation. 
 
- There are no privacy concerns because the data that is analysed is publicly available on the social media platform tike twitter. 
 
- The social impact takes place every now and then, though the data or the timeline of the data that this project is covering is for the year 2020 and 2021 specifically and comparing it with the other previous years when COVID did not hit the world. 

- The cultural impact takes place in the setting of the USA and the immigration rules change due to the result of recession. 

- It is important for the upcoming international students and immigrants to have the knowledge about how trend and immigration rules change owing to the change in the world economy and infrastructure. They should have a clear view and idea about how their life can be affected in a positive or a negative way as a result of recession. 

- Specially for the part or the community which has a big part or percentage in the society to play, ML should have specific tools predefined, that could suggest and guide people based on the sentiments of society to a specific scenario, so that instead of getting false information from wrong resources, ML can be used as a valid resource to look forward to when such situation occurs. 

## REFERENCES:

* https://towardsdatascience.com/try-texthero-the-absolute-simplest-way-to-clean-and-analyze-text-in-pandas-6db86ed14272

* https://docs.cloudera.com/documentation/enterprise/6/6.3/topics/cm_mc_solr_service.html                  

* https://spark.apache.org/sql/
 
* https://www.tutorialspoint.com/spark_sql/spark_sql_dataframes.html

* https://docs.cloudera.com/runtime/7.2.7/search-managing/topics/search-updating-the-schema-in-a-solr-collection.html

* https://github.com/dsuarez993/bigdata-realtime-twitter-analysis

* https://github.com/6vedant/TwitterAnalyticsHadoop

* https://www.toptal.com/apache/apache-spark-streaming-twitter

* https://hadoop.apache.org/


