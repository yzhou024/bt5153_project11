# bt5153_project11
**BT5153 Group Project - Group 11**

The purpose of this project is to **predict standard cost fee** for those streaming service platforms who has only launched in a few countries, what the subscription fee should be set when entering the new market where Netflix has launched given the resources they owned and how to ensure the competitiveness of the pricing strategy. Included in the GitHub repository are the datasets and notebooks for all models run.

The original datasets can be found below. All other relevant references have been cited in the project report11.

	Netflix subscription fee Dec-2021: https://www.comparitech.com/blog/vpn-privacy/countries-netflix-cost/
	dataset_country_level_others: 
		1)https://en.wikipedia.org/wiki/List_of_countries_by_number_of_broadband_Internet_subscriptions 
		2)https://ourworldindata.org/ 
		3)https://data.worldbank.org/ 
		4)https://dmerharyana.org/world-happiness-index/ 
	weekly_top_10: https://www.kaggle.com/datasets/mikitkanakia/netflix-top-10-weekly-dataset



**Project Stages**

**Stage 1:** Data Preprocessing and Feature Generation/Selection

Used pandas to collate over 65 individual unique values and combine the datasource from below 5 files: 

    Netflix subscription fee in different countries: netflix price in different countries.csv 
    Netflix subscription fee till Dec 2021: Netflix subscription fee Dec-2021.csv
    IMDb rating and TV show episode data: Please go to https://datasets.imdbws.com/ and download title.basics.tsv.gz & title.episode.tsv.gz (due to size limiation, it cannot be updated in Githut repo)
    Country-level Metrics: dataset_country_level_others.csv
    Weekly top 10 watches in Netflix: all-weeks-countries.csv

Identified Total Library Size, No. of TV Shows, No. of Movies, Movie_aveRating, TV_aveRating, GDP, Population, Gini_Index, Happiness_Share, Life_Satisfaction,Broadband_subscriptions, Cellular_subscriptions, averageRating, numVotes as the features in explaining the variation in predicting Cost Per Month - Standard ($).

Code file: 

	Generate Country Level Metric with original dataset - code11_1_country-level_metrics.ipynb;
	Add Country Level metirc with data preprocessing - code11_2_DataPreprocessing_includingCountry.ipynb;
	Add top 10 watches in Netflix - code11_3_top10_data_pre.ipynb


Output final raw data file:

	raw_0419_late.csv


**Stage 2: Train Test Slipt**

Slipt train and test data as 20% ratio to ensure all models using the datasets. 

Code file: 

	code11_combine_data.ipynb

Output file: 

	1)train.csv  
	2)test.csv


**Stage 3: Different Models**

Used Random Forest, LightGMB, XGBoost and Neural Network modelling to predict Standard Cost across each customer.
Trained regression models on the train.csv dataset and tested against the test.csv dataset.


Code file: 

	code11_RandomForest.ipynb
	code11_LightGBM.ipynb
	code11_xgboost.ipynb
	code11_neural_network.ipynb
	



**Stage 4: Final Model & Prediction**

Regression-based random forest showed the best performance, with a mean absolute error of xx ..



