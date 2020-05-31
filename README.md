# Zomato-Restaurants-Analysis
This project is about Analysing the restaurants in Bangalore which are listed on Zomato. The Dataset has been taken from https://www.kaggle.com/himanshupoddar/zomato-bangalore-restaurants

The dataset contains 17 features for giving the info about nearby 12k restaurants such as type, location, cuisines, reviews etc.
The more information about dataset can be found on the link given above.

## Analysing the Restaurants:
Opening a restaurant in a city like Bengaluru will never be easier as it used to be in the past because of the several obvious reasons. Bengaluru, being an IT capital of India, has more than 12,000 restaurants with restaurants serving dishes from all over the world. Most of the people here are dependent mainly on the restaurant food as they don’t have time to cook for themselves.

In order to help people/our client who want to open new restaurant or they would want to bring a change in their existing restaurant to compete in the market, we can analyse several factors.

We'll perform analysis using the data, by studying the factors such as:

• Location and types of the restaurant  
• Approx Price of food  
• The needs of people who are striving to get the best cuisine in the city  
• Services provided by them  
• Reviews and Ratings  

### Preprocessing the Data:
We'll see how much of the restaurants entries contain actual information and how much of it us Null. We then remove number of features which we see as redundant information as it won't help in analysis, such as Phone number.

### Analysing the features:
We take a look at the distribution of costing feature here..

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Disribution%20of%20Approx%20cost%20for%202.png)

The Distribution of the 'Approximate Cost' parameter is right-skewed. The distribution shows most of the restaurants offer food at rates upto 1000 INR for 2 people.

We will try to answer the following questions using our data:  
How much is the average approx cost for two in bangalore?  
In which area, there are highest number of restaurants? Location wise restaurants density..  
Location wise approx cost for 2..  
Location wise restaurants which have both online order and table booking available..  

We've found that Average approx cost for 2 of overall restaurants in Bnagalore is 500-600 INR.  
Number of restaurants location wise, we'll visualize using bar graph.  
But for the client's information, we can give the idea of the average cost of 2 people for each category of the restaurants.

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Restaurants'%20Category-wise%20Avg%20Cost%20for%202.png)

Although this dataset doesn't have detailed data about food items costs, it may help the client to decide on the 'costing of food items' for their restaurant, that if two people come in there, how much would it cost on an average.

We'll visualize the number of restaurants location wise. After dropping the duplicates, we now have total of around 12k restaurants. Here we are seeing the location wise restaurants distribution.

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Rest_densities.png)

The client can now get a brief idea about where can they think of opening new restaurant. They may come to the conclusion by knowing some more information further.

Some more information can be explored regarding the restaurnts like the availability of online order and table booking...
Here we can provide some more insight on the restaurants. On a particular location, how many restaurants have the Table booking, online order, both facilities, and none of those facilities available.

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/table_book_ordering.png)

We see that plenty of the restaurants provide Online ordering facility. While table booking is available at handful of restaurants.
Most of them do not provide any of these facilities.

We can also think of displaying the Geographical map and putting markers on it on the location of the restaurants as follows:

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Map%20with%20markers.png)

And Heatmap as well:

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Geo%20Heatmap.png)

### Correlation Heatmap:

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Correlation%20Heatmap.png)

We observe that there is a high positive correlation between Booking Table and Approximate Cost for two.
It implies that the cost is higher where Table booking facility is provided.

### Most liked Dishes:
We'll see what are the dishes do Bangaloreans like the most. Using Word cloud.

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Most%20liked%20dishes.png)

Seems like Biryanis, Butter Chicken, Dosa, Ice Cream are some of the popular dishes among Bangaloreans.

### Most Popular Cuisines:
Let's See what Cuisines are popular in Bangalore.

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Most%20popular%20Cuisines.png)

North Indian Cuisines are the most popular here. Not to forget about the South Indian and Chinese food though.

## Analysing the Reviews

After Preprocessing all the Reviews, We can get even more insights by showing n-grams out of reviews.

### Top keywords from Reviews:

#### Unigrams:

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Unigrams.png)

#### Bigrams:

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Bigrams.png)

### Trigrams:

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Trigrams.png)

### Sentiment analysis:

By using Keras LSTM network, we have built a model that has learnt the sentiment in the reviews and is able to predict the unseen reviews sentiments with significant accuracy of 95%.

![Link Text](https://github.com/SamSKore/Zomato-Restaurants-Analysis/blob/master/Vizualizations/Confusion%20Matrix.png)


## Conclusion:

#### To summarize from the data:
Overall there are positive reviews in majority of the restaurants in Bengaluru. Reviews also indicate that the bangaloreans are concerned about the food quality and many other things such as Ambience, overall experience, service etc. A few negative reviews also indicate that Bangaloreans are pretty much critical when it comes to go out in the restaurants to hang out.

#### About the Business Problem:
We can choose to take various decisions with our restaurant owner client on possible areas such as type of restaurant, serivices provided. We can take conclusive decisions based on the restaurant owner's budget to start a new restaurant and other preferences.
Although this data does not include several other aspects for the business problem, we've got plenty of insights for our client which will be definitely useful when they want to open a new restaurant in Bangalore.
