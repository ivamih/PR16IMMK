# PR16IMMK

## Video game sales with ratings

We have chosen a dataset from Kaggle, https://www.kaggle.com/rush4ratio/video-game-sales-with-ratings

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


** Descriptive Sctatistics **
 | Name | Platform | Year_of_Release | Genre | Publisher | Developer | NA_Sales | EU_Sales | JP_Sales | Other_Sales | Global_Sales | Critic_Score | Critic_Count | User_Score | User_Count | Rating 
------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------
count |
unique |
top |
freq |
mean |
std |
min |
25% |
50% |
75% |
max |

**Goals**


<sup>1</sup>Metacritic is a web site that collects reviews about a variety of music albums, video games, movies, series, etc. Finally, for each product, two average scores are calculated, one of the analysts in Metacritic, another from the subcribers on the site.
<sup>2</sup>ESRB(Entertainment Software Rating Board) is a non-profit organisation that assigns video games ratings and content based applications, the interctive elements it contains and the age for which it is intended.
<sup>3</sup>VG Chartz is a video game website that deals with data collections for video games, consoles and hardware.
<sup>4</sup>The attribute represents the sum of NA_Sales, EU_Sales, JP_Sales and Other_Sales. It can be removed for futher analysis or used as a summary attribute.
