jupyter notebooks
---------------
clean_data.ipynb takes a given dataset, randomly selects 200,000 entries, and cleans them

write_clusters.ipynb creates a table of the clusters of a given dataset and writes it to an excel sheet

Clusters.ipynb plots the features of botnet vs regular flows, performs k-means clustering on a given dataset, calculates silhouette values


read_data
---------------
--the original data obtained from the CTU-13 site--

read_data/read_data_(1-4).csv contains the full chart of features for the CTU-Malware-Capture-Botnet-(42-45) datasets. 


working_data
---------------
working_data/data.csv contains the reduced dataset of features for the Neris 42 dataset.

working_data/botnet.csv contains all the botnets in data.csv

working_data/benign.csv contains all the benign flows in data.csv

working_data/no_outliers contains the dataset of features with outliers removed

working_data/clusters_chart.xls is a table of each type of malware/non-malware in each cluster when dataset 42 has been put into 30 clusters


results
----------------
results/k-means scores.txt is a list of the silhouette scores for varying numbers of clusters for datasets 42-46

results/centroids.txt is the list of centroids for dataset 42 when k-means clustering has been performed for 10, 20, 30, 40, and 50 clusters

results/dataset42_clusters_visualization is a graph of the types of malware/non-malware within each cluster when dataset 42 is grouped into 30 clusters. Blue represents non-malware and red represents malware.
