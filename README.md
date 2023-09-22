# Clustering Analysis for Transactional Data

This project involves the analysis of transactional data, focusing on clustering analyses to categorize different transactions. The primary objective is to identify transactions labeled as 'Urgent' based on various features, such as drop-off and pick-up locations, price, distance, and time.

## Description

The project uses two clustering algorithms: K-Means and DBSCAN. K-Means is used for initial analysis, dividing the data into three clusters. However, due to its limitation in handling non-spherical and irregular shapes of data distribution, DBSCAN is also employed to identify 'Urgent' orders effectively.

### K-Means
The initial analysis using K-Means algorithm results in three clusters, with some overlap in drop-off and pick-up locations. The analysis assumes that overlapping locations might have price differences and transactions with higher prices are initially identified as 'Urgent'.

### DBSCAN
Due to its high memory consumption, DBSCAN is applied to subsets of the entire dataset, divided into five groups. It effectively distinguishes outliers with significantly different prices, distances, and times, even when the drop-off and pick-up locations are the same, categorizing them as 'Urgent'.

## Libraries Used
- pandas
- numpy
- sklearn
- matplotlib

## Sections
1. Importing January Data
2. Feature Selection for Clustering: Choosing pick-up and drop-off locations, starting price, shared ride requirement, and order time.
3. K-Means Clustering Analysis
4. DBSCAN Clustering Analysis
5. Feature Selection through Covariance
6. Selection of DBSCAN 'eps' parameter

## Insights
The analyses reveal that the identified 'Urgent' orders or outliers tend to have longer distances, durations, higher prices, and additional charges, compared to normal orders, under the same pick-up and drop-off locations. These 'Urgent' orders can be targeted to identify high-value customers.

## How to Run
To run the analysis, open the `part3.ipynb` notebook in a Jupyter environment and execute the cells sequentially. Ensure that the required libraries are installed in your Python environment:

```sh
pip install pandas numpy sklearn matplotlib
