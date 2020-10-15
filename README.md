# Recommendation-Engine
IBM Watson

## Project Motivation
There are three different types of recommendations: knowledge based, content based, and collaborative filtering. In this project I've decided to implement collaborative filtering to recommend items to users. Neighbourhood based collaborative filtering uses the connections between simliar users and their interactions with items to make recommendations. Similarity can be determined from the popular metrics: Pearson's correlation, Spearman's correlation, Kendall Tau's correlation, Euclidean distance, or Manhattan distance. Depending on the data we have to choose the right similarity metric. We can infer what users would like and test our predictions using as you will see.

## Project Description
In this project, I will use data from IBM Watson to make article recommendations to users on the IBM Watson Studio platform. This will be accomplished by cleaning dataframes and making a user item matrix which records user interactions. The user item matrix can then be used to find similiar users. I made a final recommendation engine which recommends the most popular articles from the most similiar users and fills any missing recommendations from the top articles making sure no articles are repeated recommendations. I then test my recommendations splitting the original data into training and testing sets to see how many latent features are needed to make accurate recommendations.

## File Description
The dataset for this project originates from IBM Watson. The data I investigate here consists of small changes to the original dataset, such as removing duplicates and mapping the email to a user id and removing the email column. 

>Recommendations_with_IBM.ipynb: detailed analysis report<br>
>articles_community.csv: contains article data <br>
>user-item-interactions.csv: contains user interactions data with articles <br>
>project_tests.py: known solutions for comparison <br>

## Results

I was able to make several conclusion based on my reccommedation engine: <br>

* The algorithm had an accuracy of 96-98% based on the number of latent features for the testing data which is pretty good
* The more latent features I trained my algorithm on, the lower accuracy score I get on my testing set
* Due to the low number of users in the testing set, my algorithm was overfitting the predictions 

In conlcusion I made a recommendation engine which would improve how users find articles on the IBM Watson Studio platform.

