# ICCS23Data
Data from our ICCS 2023 paper on using random forests to predict ABM results.

If using this data, please cite `M. Olsen, M. Raunak, D.R. Kuhn. Predicting ABM Results with Covering Arrays and Random Forests. Proceedings of the 2023 International Conference on Computational Science, June 2023.`

## What is the Data?

The data in this repository is the result of running Wilensky's HeatBugs simulation across about 4 million parameter combinations (4,005,551). Each parameter combination was run 4 times with different random number seeds. We used this data to demonstrate that it was feasible to train a random forest machine learning model on a small subset of the data to then predict a larger subset of data.

The parameter combinations were generated using covering arrays, as detailed in the above paper: a 2-way covering array, and 3-way covering array. This data is separated for the purpose of our study, but as they are of the same format with no duplicate parameter combinations they could be combined for a different study.

## Data Files

There are two data files in this repository.
