# PR16IMMK

## Video game sales with ratings

We have chosen a dataset from Kaggle, https://www.kaggle.com/rush4ratio/video-game-sales-with-ratings
**Goals**

**Data** 

The data set consists of video games, information on their sales and ratings received by Metacritic<sup>1</sup> and ESRB<sup>2</sup>. The basic data and sales data are taken over by VG Chartz<sup>3</sup> and are then complemented by ratings from Metacritic and ESRB. Only games that are sold in more than 100000 copies are included.

Attribute | Description      | Type | Value
----------|------------------|------|------
Name      | Name of the game | String | Discrete
Platform | Console on which the game is running | String | Discrete
Year_of_Release | Year of release | Numeric | Discrete
Genre | Genre |  String | Discrete
Publisher | Company that publishes the game | String | Discrete
NA_Sales | Game sales in North America in millions of units | Numeric | Continuous
EU_Sales | Game sales in Europe in millions of units | Numeric | Continuous
JP_Sales | Game sales in Japan in millions od units | Numeric | Continuous
Other_Sales | Game sales in the rest of the world, i.e. Africa, Asia excluding Japan, Australia, Europe excluding EU and South America in millions of units | Numeric | Continuous
Global_Sales | Total sales in the world in millions of units <sup>4</sup> | Numeric | Continuous
Critic_Score | Aggregate score compiled by Metacritic staff | Numeric | Continuous
Critic_Count | The number of critics used in coming up with the critic score | Numeric | Discrete
User_Score | Score by Metacritic's subscribers | Numeric | Continuous
User_Count | Number of users who gave the user score | Numeric | Discrete 
Developer | Party responsible for creating the game | String | Discrete
Rating | The ESRB ratings (e.g.Everyone, Teen, Adults Only..etc.) | String | Discrete


**Descriptive Sctatistics**

 X | Name | Platform | Year_of_Release | Genre | Publisher | Developer 
------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- 
count | 6825 | 6825 | 6825 | 6825 | 6825 | 6825
unique | 4377 | 17 | 25 | 12 | 262 | 1289 
mean | / | / | 2007.43 | / | / | / 
std | / | / | 4.21 | / | / | / 
min | / | / | 1985 | / | / | /
25% | / | / | 2004 | / | / | /
50% | / | / | 2007 | / | / | /
75% | / | / | 2011 | / | / | /
max | / | / | 2016 | / | / | /


X | NA_Sales | EU_Sales | JP_Sales | Other_Sales | Global_Sales 
------------- | ------------- | ------------- | ------------- | ------------- | ------------- 
count | 6825 | 6825 | 6825 | 6825 | 6825 
unique | 351 | 273 | 157 | 144 | 536  
mean | 0.394 | 0.236 | 0.064 | 0.082 | 0.777  
std | 0.967 | 0.687 | 0.287 | 0.269 | 1.963  
min | 0 | 0 | 0 | 0 | 0.01 
25% | 0 | 0| 0 | 0 | 0.11 
50% | 0.15 | 0.06 | 0 | 0.02 | 0.29
75% | 0.39 | 0.21 | 0.01 | 0.07 | 0.75 
max | 41.36 | 28.96 | 6.5 | 10.57 | 82.53 


X | Critic_Score | Critic_Count | User_Score | User_Count |Rating 
------------- | ------------- | ------------- | ------------- | ------------- | ------------- 
count | 6825 | 6825 | 6825 | 6825 | 6825 
unique | 81 | 106 | 89 | 875 | 7  
mean | 70.27 | 28.93 | / | 174.72 | /  
std | 13.86 | 19.22 | / | 587.42 | /  
min | 13 | 3 | / | 4 | / 
25% | 62 | 14 | / | 11 | / 
50% | 72 | 25 | / | 27 | / 
75% | 80 | 39 | / | 89 | / 
max | 98 | 113 | / | 10665 | / 

**Analysis**

Pre-processing the Data

Before we make a pre-processing, the set has 16719 samples. Once the samples are removed that have no values for some attributes (most often because Metacritic does not cover all platforms, so we have no grades for everyone), there are approximately 6900 items. From these, we are discarding games for which we do not have a year of release, and finally, 6825 instances remain with all the attributes. We think that these are enough instances to work with the set. However, this causes us to lose a large part of the games before 1999 (before Metacritic is formed) because a small part of these games have all the attributes. Additionally, as seen in the graph for the year of production there are several years after the formation of Metacritic for which we do not have data at all. For these reasons, we kept the original set in case we need the data in the future work.

Year of Release
![picture](D:\Jupyter Notebooks\Video Game Sales with Rating\Year_of_Release.jpg)


<sup>1</sup>Metacritic is a web site that collects reviews about a variety of music albums, video games, movies, series, etc. Finally, for each product, two average scores are calculated, one of the analysts in Metacritic, another from the subcribers on the site.

<sup>2</sup>ESRB(Entertainment Software Rating Board) is a non-profit organisation that assigns video games ratings and content based applications, the interctive elements it contains and the age for which it is intended.

<sup>3</sup>VG Chartz is a video game website that deals with data collections for video games, consoles and hardware.

<sup>4</sup>The attribute represents the sum of NA_Sales, EU_Sales, JP_Sales and Other_Sales. It can be removed for futher analysis or used as a summary attribute.
