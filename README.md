# spark-sql-spark-ml
This repository contains spark sql functions and spark ml functions

# Users Manual

Initially, activate virtual environment as shown below and displayed in Figure 1. 

•	Open bash and direct to main folder.

•	Switch to python 3 with following command:

   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o	scl enable rh-python36 bash
    
•	Create virtual environment:

   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o	pipenv install
    
•	Start Jupyter Notebook by:

   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o	pipenv shell
    
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;o	jupyter lab
    

 
## Task 1.

•	First group data by region and channel (after completing importing necessary libraries and data). 

•	In the grouped elements; aggregate count, average Fresh products, average Grocery products and average Frozen products.

•	Order by region to see table in order.
 
The resulting table is as follows:

![image](https://user-images.githubusercontent.com/29654044/124645698-6a066300-de9c-11eb-86da-b86be49f6de5.png)


Even though, rates can change, second channel has higher average annual spending on Grocery products and on every region as above. Fresh and Frozen products have higher average for the channel 1. So, if we assume that Fresh and Frozen products are generally consumed at hotels, restaurants and cafes, channel 1 is probably the Horeca channel. And if we assume that grocery products are bought at retail places, channel 2 is probably the retail channel.

Also there are differences in regions, too. If we consider that all regions have different geographical, economical features, it is expected to see some differences on average spending of products.

 
## Task 2. 

•	Import necessary libraries.

•	Extract features that will be clustered.

•	For kMeans, generate features column as input column.

•	Scale data and set results into another column (“norm_features”).

•	Run KMeans algorithm in a for loop to see results of different k values.

![image](https://user-images.githubusercontent.com/29654044/124645487-29a6e500-de9c-11eb-9273-aa2795585ad4.png)



## Based on these results, which K value would you choose and why?

The cost will keep decreasing as cluster number increases. Thus, we should find an optimal k. We could follow elbow method to decide optimum k value. I checked results with k = 6 and cost was around 442. Cost difference at next k values were around 200 – 300 at the beginning. I think I choose k=5 for optimal k value considering that cost difference of next k value is around only 44. It could be acceptable as the elbow curve point which also could be visible in the Figure 4 shown below.
  

 ![image](https://user-images.githubusercontent.com/29654044/124645401-0f6d0700-de9c-11eb-9693-65cfe8d994d7.png)


