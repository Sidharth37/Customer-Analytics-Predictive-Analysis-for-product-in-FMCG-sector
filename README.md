# Customer-Analytics-Predictive-Analysis-for-product-in-FMCG-sector

The main aim of the project is to identify key price points in the market, define customer segments, develop new pricing strategies based on competitive intelligence to capture the most possible market share and in turn maximize revenue. With the advent of online shopping, the data to make this happen has become increasingly possible, and something everybody is cashing on. In this project we have made an effort to analyze the probability of customers of buying a particular product from a product segment, probability of customer of buying a specific product brand, and the number of units a customer would buy.<br>

A full scaled project of this type is divided into 3 phases<br>
1. Segmentation
2. Targeting
3. Position <br><br>

We will be focusing on the segmentation and positioning part of it. Targeting is something that would require you to focus on the no quantitative part of the exercise, and is beyond the scope of the project.<br><br>
<b>Segmentation -</b>
The main aim of this phase to derive distinctive consumer segments. Consumers in a particular segments are supposed to be as similar to each other as possible, where as consumers in different segments need to be as different as possible. We will carry out the segmentation exercise based on customer demographic information - sex, marital status, age, education, income, occupation and settlement size.<br>
After the inital exploratory data analysis, we start by pre processing data to get rid of biases of scales and measurements. A quick hierarchical clustering is the most effective way to find out the tentative numbers of clusters we could expect to see, in our case this comes out to be 4.<br>
Once we have this approximation, we start with k-means clustering. The 1st step is to calculate WCSS(within cluster sum of squared distances) in the range around the approximation. The number of clusters should have based on WCSS comes out to be in agreement with the earlier value of 4 we had approximated. At this stage we start with the actual clustering. At this stage we move on to looking at the seperation between clusters, to verify that there isn't an overlap. Based on statistical analysis and visualization we see that there is some amount of seperation, with some scope for improvement.<br>
At this stage, we go back to origanl preprocessed data, an implement PCA(Principal Component Analysis). After this we go through a similar series of steps as we had executed earlier and reach to astage where we have 4 clusters with the seperation we were aspiring for.<br>
Based on the variable distribution of each principal component and the correlation with the 3 principal components we have chosen the 4 clusters we get are - <br>
a. Cluster 0 - Struggling individuals<br>
b. Cluster 1 - Career Driven individuals<br> 
c. Cluster 2 - Standard individuals<br>
d. Cluster 3 - Well off individuals<br>

Once we have the clusters formed, the next stage is targeting, since it is out of scope for this project, we will move on to positioning.<br><br>
<b>Positioning -</b><br>
In this phase we will answer question related to product type purchase probability, brand purchase probability and purchase quanitity.<br> 
<b>This phase is carried out in 2 parts:</b><br>
i  Exploratory data analysis<br>
ii Modeling<br>

<b>Exploratory data analysis -</b><br>
In this stage we try to understand the customer base belonging to each segment, the average number of store visits a customer from each segment makes, the average number of purchases belonging to the product type of interest a customer makes, the average purchase quantity a customer of each of these segments make.<br>
The next stage is to the correlation of customer segments to buying a paritcular brand, this tells us the affinity certain segments have towards certain brands.
After this we explore the revenue each segment makes for each of the particular brand. To sum up everything the we start to understand the choices made by customers of various segments, at the same time we understand the segments which contribute heavily to each individual brand.<br><br>
<b>Modeling</b><br>
At this stage we start by computing price elasticity, at this stage we compute price elasticity in general rather than for a parituclar brand. We try to understand the effect of price with respect to the outcome of sale. Once this is computed we move towards computing the price elasticity for each particular segment. Using this we can determine the cross over point for each segment. The cross over point is the point at which increase in price leads to subsequent decrease in sale quanitity to a level that it brings the revenue down. Also as expected the segment most affected by price is the struggling segment and the segment least affected by price fluctuations is the well off segment. After this we move on determine the price elasticity and cutoff points with and without promotions. At this stage we realize that the cut off values are generally higher when there is a promotion rather than when there isn't. This tells us that consumers are less likely to be affected by incremental price fluctuations when there are promotions running. For the final part of this stage we determine the effect price fluctuations for our brand of interest in 2 scenarios, the 1st one being keeping competitors price constant and changing our prices, and the second one keeping our price constant, while changing the competitors pricing. 

