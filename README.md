# Analyzing Ecommerce Customer Data For Insights 

## We will be using the following Statistical & ML Models to accomplish our objectives

Analyze online shoppers' purchase intentions using Logistic Regression, K-means clustering &amp; A/B Testing
- Logistic Regression
- K-Means Clustering
- A/B Testing
- Vizualization

## Outlining the Approach 

From online shopping dataset, we will be trying to draw insights from a customer's behavior on the site.
We will analyze a number of factors, such as conversion rate and total revenue generated.
We will also perform univariate and bivariate analysis while taking various dataset features into consideration,
such as pageview duration, types of visitors, types of traffic, and browsers used. 
Then, we will implement the K-means algorithm and elbow method to find the optimum value of clusters, and visualized scatterplots
based on this value. These plots, in turn, provide us with useful information so that we can plan our next course of action.

## Summary of Insights

At the very outset lets check if there is statistical difference between *visits with transaction and visits without*. <img width="505" alt="Screenshot 2023-01-22 at 10 09 31 PM" src="https://user-images.githubusercontent.com/80999165/213960022-fc3868a0-7609-4ca3-ab56-34906d4d1e8d.png">

Last column with ttest pval contains the signifance value, and we can see that except Region, Traffic Type and Operating system all other features are 
significantly different between Visit with Transaction and Visits with no Transaction. Its a good place to start analyzing our dataset. 

**Correlation Between Bounce Rate vs Exit Rate**

  As you can see, there is a positive correlation between the bounce rate and the exit rate. With the increase in bounce rate, the exit rate of the page increases.

<img width="864" alt="Screenshot 2023-01-22 at 10 41 24 PM" src="https://user-images.githubusercontent.com/80999165/213962409-52496e95-28ae-461a-a1a6-a9355eb02a4b.png">

**Page Value Versus Bounce Rate**

<img width="865" alt="Screenshot 2023-01-22 at 10 41 46 PM" src="https://user-images.githubusercontent.com/80999165/213962809-1ae9f8cf-ff48-44c7-ac75-f02249918b51.png">

As we can see in the preceding plot, there is a negative correlation between page value and bounce rate.
As the page value increases, the bounce rate decreases. To increase the probability of a customer purchasing with us, we need to improve the page value—perhaps 
by making the content more engaging or restructuring the content.



**Modeling the Relationship Via Logistic Regression**

Logistic Regression is excellent way of estimating the relationship between m different features when the target variable is binary - Transaction and No 
Transaction. 

We use Statsmodel to run Logistic regression after converting categorical features with into dummy variable and dropping the first to prevent 
multi collinearity. 

We get the following output
<img width="815" alt="Screenshot 2023-01-22 at 11 05 34 PM" src="https://user-images.githubusercontent.com/80999165/213964235-31919c72-573b-46f8-ad1d-ced7f5b8e0b6.png">

 
