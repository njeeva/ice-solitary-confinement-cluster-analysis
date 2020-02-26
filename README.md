# What are characteristics that define how long ICE detainees spend in solitary confinement?

A cluster analysis was performed on data from the [International Consortium of Investigative Journalists](https://www.icij.org/investigations/solitary-voices/how-us-immigration-authorities-use-solitary-confinement/) on the use of solitary confinement on immigrant detainees by U.S. Immigration &amp; Customs Enforcement. The average length of stay in solitary confinement was appproximately 35.5 days with a standard deviation of 56 days. Detainees were clustered based on their length of confinement and similarities within the groups were analysed. 

From the analysis, 4 clusters emerged, with stays around 6, 27, 60, and 158 days in solitary confinement. The cluster nodes and number of individuals in each cluster is detailed in the table below.

![Cluster Table](https://github.com/njeeva/ice-solitary-confinement-cluster-analysis/blob/master/Cluster%20Node%20Table.JPG)

### Data Interpretation

Across the four clusters, a number of similarities and differences can be seen. The confinement facilities, the citizenship data, the date of placement/release, and the given reason for placement can be seen for each record. Trends in these changes avross each cluster was analyzed using pivot tables. This information is very useful for quiding activists trying to hold ICE accountable. Images belows show the detainee citizenship make up of cluster 1 (with a central node of 6 days in confinement) and of cluster 2 (with a central node of 158 days in confinement). While those of Mexican nationality made up 29% of cluster 1, this percentage rose to 42% of those in cluster 2. Mexican detainees are much more likely to be detained in solitary confinement for many more days than those of other nationalities. Information like this can help ICE officials, regulators, and activists run investigations into the reasons for these discrepancies, and design programs to retrain agents.

![Cluster 1](https://github.com/njeeva/ice-solitary-confinement-cluster-analysis/blob/master/Cluster%201%20Citizenship.JPG) ![Cluster 2](https://github.com/njeeva/ice-solitary-confinement-cluster-analysis/blob/master/Cluster%202%20Citizenship.JPG)

### Step by Step Analysis
1. Download the initial data set.
2. Insert rows at the top of the excel sheet and calculate the average length of confinement and standard deviation of the data. With this information, calculate the z-score for each record.
3. Predict 4 cluster nodes and record the ID, days in solitary confinement, and z-score for each using the VLOOKUP function. 
4. Calculate the distance between each record and the predicted cluster nodes and determine which node is closest to each.
5. Sum together the minimum distances for each.
6. Using the solver function on excel, vary the predicted nodes until the sum of distances is at a minimum.
7. From this, the actual cluster nodes have been determined. Create pivot tables on this data in order to analyze characteristics of each cluster.
