# Customer-Segmentation-using-Unsupervised-Learning-Algorithm

**[Mall Customer Segmentation Data Set](https://www.kaggle.com/shwetabh123/mall-customers)** : Let's imagine you're owning a supermarket mall and through membership cards, you have some basic data about your customers like Customer ID, age, gender, annual income and spending score, which is something you assign to the customer based on your defined parameters like customer behavior and purchasing data.

The main aim of this problem is learning the purpose of the customer segmentation concepts, also known as market basket analysis, trying to understand customers and sepparate them in different groups according to their preferences, and once the division is done, this information can be given to marketing team so they can plan the strategy accordingly.

**Data Set Information**  

This dataset is composed by the following five features:

* CustomerID: Unique ID assigned to the customer
* Gender: Gender of the customer
* Age: Age of the customer
* Annual Income (k$): Annual Income of the customer
* Spending Score (1-100): Score assigned by the mall based on customer behavior and spending nature.


In this particular dataset we have 200 samples to study.

To visualize our data and plot important information so we can see the different values our data has and its behaviour. To do so, we are only going to consider the following features: Annual_income and Spending_score. 

In this project we will focus on 2 types of clustering method which is **K-Means Clustering** and **Hierarchical Clustering** method. Both will be using the same data set an we will compare the result.

# K-Means Clustering

In this project, we are only going to consider the following features: Annual_income, Spending_score and Age. Firtsly, we need to decide the amount of clusters we want to divide our data in. To do so, we are going to use the Elbow Method.

![](https://github.com/Asmuie/Customer-Segmentation-using-Unsupervised-Learning-Algorithm/blob/main/images/kmeans_elbow.png)

The elbow method is used to determine the optimal number of clusters in k-means clustering. The elbow method plots the value of the cost function produced by different values of k and one should choose a number of clusters so that adding another cluster doesn't give much better modeling of the data. In this problem, we are using the inertia as cost function in order to identify the sum of squared distances of samples to the nearest cluster centre.

Looking at this particular example, if we imagine the line in the graphic is an arm, the elbow can be found, approximately, where the number of clusters is equal to 5. Therefore we are selecting 5 as the number of clusters to divide our data in.


In the process of clustering we will not be considering the gender factor anymore. The first main reason of why we do take this approach is because the difference between male and female in this data is not particularly high and making a gender differentiaton won't provide any further information. The second and not least important reason is the fact that stores, in general, hardly ever target a specific gender anymore, in almost every store in a shopping center male and female products can be found.

Additionally we do not want to interfere in the process of unsupervised learning, we will leave the algorithm do its job and once it's finished we will analyze the results and extract conclusions and knowledge.

![](https://github.com/Asmuie/Customer-Segmentation-using-Unsupervised-Learning-Algorithm/blob/main/images/kmeans_result3d.png)


After plotting the results obtained by K-means on this 3D graphic, it's our job now to identify and describe the five clusters that have been created:

Orange Cluster - The orange cluster groups young people with moderate to low annual income who actually spend a lot.
Green Cluster - The green cluster groups reasonably young people with pretty decent salaries who spend a lot.
Purple Cluster - The purple cluster basically groups people of all ages whose salary isn't pretty high and their spending score is moderate.
Blue Cluster - The blue cluster groups people who actually have pretty good salaries and barely spend money, their age usually lays between thirty and sixty years.
Red Cluster - The red cluster groups whose salary is pretty low and don't spend much money in stores, they are people of all ages.

# Hirarchical Clustering
