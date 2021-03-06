# EEML_Final_Project_Crypto

## Useful Links
- project drive: https://drive.google.com/drive/folders/13ueTjXCT1uD0yghKgkTdWN6uVQ0Ru99P?usp=sharing
- Kaggle tutorial: https://www.kaggle.com/cstein06/tutorial-to-the-g-research-crypto-competition
- feature engineering md: https://hackmd.io/wurSzyc5RyKJ_tiJnWQMpg
- report/presentation structure: https://docs.google.com/document/d/1407GC_CDIjMhYRu-AsMAwVK2ShO7OAlKwXhhdTO9S34/edit?usp=sharing
- 0102 meeting notes: https://docs.google.com/document/d/1W8sWToLrOlfixD2aWEyJPW4ww1qCw0LfdGHJo1a4cUs/edit?usp=sharing


## Feature engineering
- Please refer to `DataPreprocessing.py`, `FeatureEngineering_tutorial.ipynb`(storing the results)
- feature engineering steps
    - load data
    - preprocess for timestep
    - whehter to load strict data or not
    - slice by asset id
    - fill missing timestamp (sue forward filling from tutorial notebook, may try different methods in experiment)
    - create different technical analysis features with different parameter sets

## Feature selection
- Please refer to `FeatureSelection.py`, `FeatureEngineering_tutorial.ipynb`(storing the results)
- feature selection steps
    - L1 regularization regression
        - tunable params: nubmer of cv, max_iter (won't change result too much)
    - correlation coefficients 
        - tunable params: threshold on correlation, (or may just set a upper bound on number of selected features) 
    - union features selected by the two above methods