Problem statement- 
HELP is an  NGO, committed to fighting poverty and providing backward countries with basic amenities and relief during the time of disasters and natural calamities. 
The CEO of the NGO needs to decide how to use money strategically and effectively. 
The significant issues that come while making this decision are mostly related to choosing the countries that are in the direst need of aid.

Business Goal-
To categorise the countries using some socio-economic and health factors that determine overall development of the country. 
The model created will suggest the top 10 countries which need the NGO's help the most. This will help the NGO to decide where to use their money and resoures.

Solution Approach- Started with data cleaning, then a detailed analysis of the dataset to find the co-relation between different columns of the dataset. Analysis is done by plotting scatterplots and heatmaps.

Then divide the countries into different clusters using KMeans algorithm. 

One of the clusters will have the countries in the most dire need of help from the NGO. This will be the cluster with countries having least GDPP, leave income, max inflation.

Result- According to the model created, the 10 countries which need the NGO's help the most are-
Myanmar,Burundi,Afghanistan,Nepal,Liberia,Malawi,Comoros,Gambia,Guinea and Kenya

Detailed step by step solution desciption-
167 countries are decribed using the following columns-
country        Name of the country
child_mort   Death of children under 5 years of age per 1000 live births
exports         Exports of goods and services. Given as %age of the Total GDP
health          Total health spending as %age of Total GDP
imports        Imports of goods and services. Given as %age of the Total GDP
Income        Net income per person
Inflation      The measurement of the annual growth rate of the Total GDP
life_expec    The average number of years a new born child would live if the current mortality patterns are to remain the same
total_fer       The number of children that would be born to each woman if the current age-fertility rates remain the same.
gdpp            The GDP per capita. Calculated as the Total GDP divided by the total population.
Steps followed-
1. Import the required libraries and load the dataset.
2. Remove rows with null values and  duplicate rows.
3. Percentages do not show the real picture so converting these columns (exports,imports,health) to actual values.
4. Remove ouliers.
5. To see the corelation among different features, draw a heat map/correlation matrix.
6. Make scatterplots to see the co-relation among different features. Like graph of Income vs Child mortality vs total Fertility,  Income vs Health spending vs GDP etc.
7. Find the top 5 countries which are doing worst in the given metrics- Countries with worst child mortality rate, Countries with least exports, Countries with least health spending. 
    Similarly do the same for all remaaining columns as well.
8. Standardize the data using StandardScaler.
9. Find the optimum number of clusters using the elbow method.
10. Optimum number of clusters turns out to be 3 so divide the dataset into 3 clusters using KMeans CLustering algorithm.
11. Plot sctterplots to visualize the 3 clusters in terms of different features. 
12. Create 3 new dataframe for the 3 clusters.
13. See the mean value of each feature in the 3 clusters.
14. Cluster 1 has low income,low GDP,highest inflation,highest fertility,lowest export,lowest imports,highest inflation. 
      So countries in this cluster need to help of the NGO.
15. Sort the cluster 1 according to lowest income,lowest GDP, highest inflation,highest fertility,lowest export,lowest imports,highest inflation.
16. After sorting, get the top 10 counries of this cluster.
      These are the top 10 countries in the most dire need to help from the NGO.
According to the model created, the 10 countries which need the NGO's help the most are-
Myanmar,Burundi,Afghanistan,Nepal,Liberia,Malawi,Comoros,Gambia,Guinea and Kenya
