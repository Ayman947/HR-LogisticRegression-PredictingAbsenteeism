# HR-LogisticRegression-PredictingAbsenteeism
# Clustering-NYC-Toronto-Neighborhoods

- This project approaches a commonly faced problem by people who have to **move** from **NYC** to **Toronto** or Vice versa.

- The problem they face is that they have to move yet they prefer to move to a **similar place** to where they are, having the same **lifestyle**. (ex: similar places, similar venues, ...etc.)

- So, we **clustered the neighborhoods** within the two cities according to their most common **venues** into **6 clusters**.

- Having clustered them, people will be able to **identify easily where to go** as simple as looking at the **clustered neighborhoods map** which has been generated and identify simmilar neighborhoods by **colors**.

- [Additional **Dashboard** for interactive exploring](https://public.tableau.com/views/NYC-Toronto-Clustered-Neighborhoods/Dashboard5?:language=en-US&:display_count=n&:origin=viz_share_link)



# **Environment** & **Packages**


| Package Name | Functionality or Usage purpose |
|---------------|-------------------------------|
| Pandas        | Data Manipulation              |
| numpy        |  Numerical calculations and array manipulations   |
| json        | Handling Json Files       |
| BeautifulSoup        | Web scrapping              |
| requests        | Building APIs          |
| matplotlib        | Data Visualizatiom        |
| seaborn        | Data Visualizatiom         |
| Follium        | Geospatial Data Visualization   |
| sklearn        | Machine learning algorithms           |



# **Data Sources**

- [**NYC**-data from **Json** file](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0701EN-SkillsNetwork/labs/newyork_data.json)

- [**Toronto-data**, web scrapped from](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M)

- [**Geospatial data from** **Geospatial_Coordinates.csv**](https://github.com/Ayman947/Clustering-NYC-Toronto-Neighborhoods/blob/main/Data-Sources-Files/Geospatial-Coordinates.csv)




# **Data Cleaning** & **Preprocessing**

- Dropping unneeded columns.
- Filtering Canada data to get only Toronto's. 
- Adding longs and lats to Toronto's data.
- Appending both of Toronto's and NYC's data.
- One-hot-Encoding venues for further processing (i.e building K-Means clusters)




# **Modeling**

- We applied the K-Means algorithm which is a **partitioning** **unsupervised** clustering ML model by which we cluster a given set of observations, neighborhoods in our model, according to their features, respective venues appearence likelihood in our model, into **non-overlaping** clusters without any **internal structure**.

- We clustered the neighborhoods into 6 clusters to minimize the within-cluster sum of squares (i.e WCSS) as reasonale as possible.
![WCSS](https://github.com/Ayman947/Clustering-NYC-Toronto-Neighborhoods/blob/main/Insights-Related-Files/WCSS.png)





# **Insights** 

| Cluster _no | NYC_Cluster_Volume | NYC_Cluster_%	| Toronto_Cluster_Volume | Toronto_Cluster_% |
|---------------|-----------------|----------------|--------------------|------------------------|
|  1           |      8              |         2.62%         |           1       |      2.56% |
|   2          |       1             |          0.33%        |           -       |        -           |
|    3         |        106            |          34.75%	        |     35             |   89.74%   |
|     4        |           3         |       0.98%	           |       2           |       5.13% |
|      5       |            21        |       6.89%	           |        -          |      -            |
|       6      |              166      |       54.43%	           |       1           |     2.56%              |

> The vast majority of NYC's neighborhoods fall in the 6th & 3rd clusters.

> The vast majority of Toronto's neighborhoods fall in the 3rd cluster which we gonna describe very soon.

> In Toronto, there are no neighborhoods fall into neither the 2nd nor the 5th clusters.

> (i.e If someone lives  either in the 2nd or the 5th clusters in NYC, he/she won't find a similar neighborhood to move to in Toronto.)



# [**Results**](https://github.com/Ayman947/Clustering-NYC-Toronto-Neighborhoods/blob/main/NYC-Toronto-Venues-PostClustered.csv)
