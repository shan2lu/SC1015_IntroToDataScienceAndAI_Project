This project is for SC1015 Data Science and Artificial Intelligence course.

# Algorithms
1) Pandas                                                                                                                                                                     
2) Decision Tree regression
4) Random forest regression

# Dataset
Our group has chosen the movie industry dataset from Kaggle. The file consists of many variables relating to a movie including, name of movie, rating, genre, year of production, released date, score, votes, director, writer, star, country, budget, gross revenue, company and runtime.

# Problem
We will be exploring the problem : Which movie is worth investing in. By solving this question, investor are able to make better investing decision and hence able to profit. In our project, we will look at how different variables affect the profit of a movie to determine which movie to invest in.

# Notebook
Due to the nature of our problem, we can only utilise datas that are before the making of the movie. Variables such as ratings, score, votes can only be determined after the movie is make and hence we did not use those variables in our models. Other variables such as 'director', 'star','writer' are names that are hard to be used to build a model even with the help of one-hot encoding. This is because there are more than a thousand unique variable for each of the three category and encoding them leads to computational and memory inefficiency. Hence, two variables we used are 'genre' and 'budget' which showed strong correlation with 'profit'.

We started off by cleaning the data. We removed any null values in 'profit' and 'budget'. We added in two variables, one is 'profitPercentage' to present the increase in profit while taking note of the difference in budget for each movie. Another variable 'worth' which is established based on 'profitPercenatge', if the 'percentageProfit' of a movie is more than the median value, we will classify that movie as worth. We used mainly decision tree and random forest to come up with our three models.

For our models, all of them will be predicting worth. The first model os uni-variate classification using genre. We first encode 'genre' using one-hot encoding before feeding it into the model. The accuracy of the model is about 55% for both train and test dataset. The accuracy is not very desirable hence we proceed to build model 2 which is random forest using genre, the accuracy of the model for train dataset and test dataset is about 55% and 56% repsectively. We decided to proceed with our model 3 which is uni-variate classfication using budget. The accuracy for the train dataset and test dataset was 58% and 56% respectively, sligtly better than the previous two model. In hope to improve on the accuracy, we increases the depth of the tree. However, when the depth exceeds 7, the model is starting to overfit as the test accuracy was decreasing while train accuracy was increasing.

In conclusion, the best model that we can use will be model 3 since the accuracy is the highest. Thrill movie seems to be doing well and able to earn the most profit out of all the genres and movie with more budget tend to have higher profit too. However it is important to note that we did not take important variables such as director, star and writer which will greatly affect the profitability of the movie into considerations in building our models. Hence better models should try to take these variables into account.

Through out the project, we practiced on different machine learning teachniques, we also learnt new techniques such as one-hot encoding to encode categorical variables and random forest.

# Contributions
1) Problem formulation : shanshan & kishore
2) Data cleaning : shanshan
3) EDA : shanshan & kishore
4) Model 1 : shanshan
5) Model 2 : shanshan
5) Model 3 : shanshan
7) Slides : shanshan & kishore

# References
1) Anderson, R. (2019, August 5). What makes a successful film? Predicting a film's revenue and user rating with machine learning. Ryan Anderson. Retrieved April 21, 2024, from https://ryan-anderson-ds.medium.com/what-makes-a-successful-film-predicting-a-films-revenue-and-user-rating-with-machine-learning-e2d1b42365e7
2) [Krish Naik]. (2019, September 12). Featuring Engineering- Handle Categorical Features Many Categories(Count/Frequency Encoding) [Video]. Youtube. https://youtu.be/MPnNC6kkNC4?si=lBXJmNnazSMZnxy-
3) SC1015 Data Science and Artificial Intelligence course. Walk-Through NoteBook For Mini-project 

