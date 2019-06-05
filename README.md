# Creating-Customer-Segments-with-Arvato
Unsupervised Learning Project of Udacity Data Scientist Nanodegree

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

The following libraries are expected to be used in this project:
- `NumPy`
- `pandas`
- `Sklearn / scikit-learn`
- `Matplotlib` (for data visualization)
- `Seaborn` (for data visualization)
The code should run with no issues using Python versions 3.*.

## Project Motivation<a name="motivation"></a>

I've learned about unsupervised learning techniques that allow me to summarize the dimensions of my data and cluster unlabeled data into groups with similar properties, it's time to apply my knowledge to some real-life data.
In this project, Bertelsmann partners AZ Direct and Arvato Financial Solutions have provided two datasets one with demographic information about the people of Germany, and one with that same information for customers of a mail-order sales company. We looked at relationships between demographics features, organized the population into clusters, and saw how prevalent customers are in each of the segments obtained.

## File Descriptions <a name="files"></a>

- `Udacity_AZDIAS_Subset.csv`: Demographic data for the general population of Germany; 891211 persons (rows) x 85 features (columns).
- `Udacity_CUSTOMERS_Subset.csv`: Demographic data for customers of a mail-order company; 191652 persons (rows) x 85 features (columns).
- `Data_Dictionary.md`: Information file about the features in the provided datasets.
- `AZDIAS_Feature_Summary.csv`: Summary of feature attributes for demographic data.
- `Identify_Customer_Segments.ipynb`: Jupyter Notebook divided into sections and guidelines for completing the project. The notebook provides more details and tips than the outline given here.

## Results<a name="results"></a>

After performing Dimensionality Reduction using PCA, 28 features retained and we can explain over 85% of the variability.

In the first principal components, we know that Number of family houses in the PLZ8 region are very important features PLZ8_ANTG3 & PLZ8_ANTG4 (positive), PLZ8_ANTG1 (negative) top 5 positive and top 5 negative

In the second principal components, we know that Personality typology is a influent factor: event-oriented(+ve), sensual-minded(+ve), dutiful(-ve), religious(-ve) are all in top 5 +ve and top5 -ve

In the third principal components, we know that another personality typology contributes a lot: +ve: dreamful, socially-minded, cultural-minded, family-minded -ve: event-oriented, critical-minded, dominant-minded, combative attitude

To apply clustering to the general population using KMeans, we decided to use 8 clusters to segment the population, because, from the curve of the average distance to centroid, we found that the elbow of the curve is around 8, which is also the turning point of the curve. 

We can describe segments of the population that are relatively popular with the mail-order company, and relatively unpopular with the company. 

These segments are relatively popular with company: 3 are much more than the public 3 - related high affinity of combative attitude, male, low financial interest

These segments are relatively unpopular with company: 5,6 are much less than the public 5 is mostly related with Personality typology especially low affinity of rational, and relative young age (ALTERSKATEGORIE_GROB) 6 is mostly related with Personality typology especially rational, and high financial interest

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Must give credit to Arvato for the data. Since the terms and conditions prohibited us from keeping the data, no data is provided in this repository.
