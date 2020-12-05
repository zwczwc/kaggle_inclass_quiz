# MSBD5001_Kaggle

#### Environment

Python: 3.8.3

Package:

pandas, datatime, numpy, sklearn, lightgbm, xgboost



#### RUN

Just open the `.ipynb` file in jupyter notebook and run all code cells, then will get the submission `.csv` file in the directory. Before running, please pay attention to the dataset path and modify as you need.

The final submission file is test.csv or final.csv. They are the same. I'm afraid of the conflict name with test data.

#### Data Preprocessing and Feature Engineering

- Average value fill missing datetime (Ineffective)

- extract year, month, day, hour,day of week from datetime
- one-hot day of week
- one-hot hour (Ineffective)
- add cross term `hour of day of week` (only good for linear model)

- add go to work/after work rush hour

- add holiday

> https://www.gov.hk/tc/about/abouthk/holiday/2017.htm
>
> https://www.gov.hk/tc/about/abouthk/holiday/2018.htm
>
> https://www.labour.gov.hk/tc/news/latest_holidays2017.htm
>
> https://www.labour.gov.hk/tc/news/latest_holidays2018.htm

- add rainstorm warning signal days, divide into yellow, red and black (Ineffective)

> https://www.hko.gov.hk/tc/wxinfo/climat/warndb/warndb3.shtml?opt=3&rcolor=0&start_ym=201701&end_ym=201812&submit=%E6%90%9C%E5%B0%8B

- add Typhoon Mangkhut

> https://www.hko.gov.hk/tc/informtc/mangkhut18/report.htm

- add MTR break down

> https://www.hk01.com/%E7%A4%BE%E6%9C%83%E6%96%B0%E8%81%9E/247480/%E6%B8%AF%E9%90%B5%E5%9B%9B%E7%B7%9A%E6%95%85%E9%9A%9C-%E6%B8%AF%E9%90%B5%E7%99%B1%E7%98%93-%E4%BA%A4%E9%80%9A%E5%B9%B9%E9%81%93%E8%BB%8A%E7%A6%8D-%E5%BC%95%E7%88%86%E4%B8%8A%E7%8F%AD%E6%99%82%E9%96%93%E5%A4%A7%E6%B7%B7%E4%BA%82



#### Models

- Ridge
- Lasso
- GradientBoosting (Good performace)
- SVR
- SGD
- ExtraTrees

- RandomForest (Good performace)

- lightGBM (Good performace)

- XGBoost (Good performace and used for final submission)



#### Methods

- CrossValidation
- GridSearch
- Ensemble Learning

