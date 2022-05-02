# Cryptocurrency Analysis
The client for this project, an investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. My goal is to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped or classified for investors. 

The data needed to be cleaned and processed in order to be fit to the machine learning models. Since there is no known output, I used unsupervised learning. To group the cryptocurrencies,I used clustering algorithms. Additionally, I included data visualizations to share my findings. 

## Visual Overview of the Process
In the following collection of images, you'll be able to see the process of clustering and visualizing the clustered data. 

### First, I read in the CSV of Crypto Data that was provided by the client. 
![Read_In_CSV](https://user-images.githubusercontent.com/93888037/166171598-b0ce90f3-6ea8-435d-9503-bae83d21f525.png)

### Next, I cleaned the data to remove any cryptocurrencies that are not actively trading, delete null rows, and dropped any rows unnecessary for clustering. Here is an example of the cleaned data frame.
![Cleaned_Data](https://user-images.githubusercontent.com/93888037/166171659-977c4b11-d722-441f-af5a-6167fe2e94b7.png)

### Next, I encoded the data in order to convert all data to integers. Finally, I scaled the data to prepare it for Principal Component Analysis.
![Encoded_Scaled_Data](https://user-images.githubusercontent.com/93888037/166171787-5de911db-8af5-4905-a3d8-756026a4b78a.png)

### Next, I used Principal Component Analysis to determine the three most important components in clustering the data. Then, I loaded this information into a dataframe.
![UsedPCA](https://user-images.githubusercontent.com/93888037/166171681-7d884622-220e-4e75-be30-01d422b84f83.png)

### Next, I analyzed the data using the KMeans method of clustering. In order to determine the appropriate number of clusters, I created an Elbow Curve. 
![UsedElbowCurve](https://user-images.githubusercontent.com/93888037/166171908-ba671d54-465d-42f4-8e6a-55fce152abc9.png)

### Next, I merged the PCA Data with my original clean data frame in order to more clearly see each currency's class (as determined by clustering). 
![Merged_Data](https://user-images.githubusercontent.com/93888037/166171850-e4bcb7f6-9263-4922-9263-63f2aa6587f8.png)

### Finally, I visualized the newly created clusters. 
1. First, I created a 3D Scatter Plot using plotly_express. 
![3dplot](https://user-images.githubusercontent.com/93888037/166172117-5c3b8564-3db0-4ced-aef2-cfe222a832be.png)

2. Then, I created a table using hvplot. 
![hvplottable](https://user-images.githubusercontent.com/93888037/166172128-bab212ed-0814-465e-a333-b4bcae853c76.png)

3. Next, I used an f string to print a quick reference to how many tradable cryptocurrencies I clustered. 
![fstring](https://user-images.githubusercontent.com/93888037/166172144-6447dc4c-c516-4f54-a5ed-692e46dfe321.png)

4. Next, I used the MinMaxScaler to scale the Total Coins Mined and Total Coin Supply columns and merged all data frames to have a comprehensive look at each currency in each cluster. 
![usedminmaxscaler](https://user-images.githubusercontent.com/93888037/166172164-5b88d9a6-d1d9-46d2-b912-48185f9ade82.png)

8. Finally, I created a 2D scatterplot using hvplot to examine where these currencies fall when Total Coin Supply is compared to Total Coins Mined. 
![2dplot](https://user-images.githubusercontent.com/93888037/166172181-7c0f1502-c9e7-4c75-ad27-0f14ccc3b021.png)
