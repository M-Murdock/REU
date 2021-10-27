jupyter notebooks
---------------
`clean_data.ipynb` takes a given dataset, randomly selects 200,000 entries, and cleans them. It can be run on a single dataset (by uncommenting the first line) or multiple (by running run_clusters.ipynb).

`write_clusters.ipynb` creates a table of the counts for malware and non-malware in each cluster (from k-means clustering) of a given dataset and writes it to an excel sheet. It can be run on a single dataset (by uncommenting the first line) or multiple (by running run_clusters.ipynb).

`run_clusters.ipynb` runs clean_data.ipynb and write_clusters.ipynb on datasets 1-13, effectively cleaning each and writing the results of k-means clustering to excel sheets.

`silhouette.ipynb` calculate the silhouette values for a given dataset

`relabel_data.ipynb` takes a csv of all the malware from a given dataset and labels them them all with the corresponding botnet family. Must be run from run_relabel_data.ipynb

`run_relabel_data.ipynb` runs relabel_data.ipynb on all of the data files

`combine_datasets.ipynb` combines datasets 1-13 (excluding datasets 9-12)

`write_clusters_botnet_families.ipynb` creates a table of the counts of each botnet in each cluster (from k-means clustering) from a combined dataset (obtained from combined_datasets.ipynb). Ignores non-malware. Saves results to an excel sheet

`write_hierarchical_botnet_families.ipynb` runs hierarchical clustering and creates a dendrogram. Then it creates a table of the counts of each botnet in each cluster (from hierarchical clustering) from the combined dataset. Ignores non-malware. Saves results to an excel sheet.

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


relabeled_data
----------------
contains datasets datasets 1-13 (excluding datasets 9-12) with botnet subtype replaced with botnet family name


combined_data
----------------
combined_dataset.csv is a single file containing datasets 1-13 (excluding datasets 9-12)

combined_clusters_chart.xls is a table showing the results of running k-means clustering on combined_datasets.csv

combined_clusters_graph.xls is a graph of the data in combined_clusters_chart.xls

hierarchical.xls is a table and graph of the results of running hierarchical clustering on combined_datasets.csv
