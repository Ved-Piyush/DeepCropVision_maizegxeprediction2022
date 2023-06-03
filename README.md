# DeepCropVision_maizegxeprediction2022

To reproduce the results follow the steps below. 

1. Run the script [Data_PreProcessing.ipynb](https://github.com/Ved-Piyush/DeepCropVision_maizegxeprediction2022/blob/main/Data_PreProcessing.ipynb). This script will create a dataset called `final_data_all_with_traits.csv` in the output_data folder. This csv file contains the joined file which has the training and the test features for all data types but genotype hybrid features. 

2. Run the script [Hybrid_Features.ipynb] (https://github.com/Ved-Piyush/DeepCropVision_maizegxeprediction2022/blob/main/Hybrid_Features.ipynb) which will create the two TensorFlow models called `first_col_pca_200` and `second_col_pca_200` which will compose the PCA embeddings for the genotype features for the hybrids.
 
3. Run the script [Train_Test_Split_Imputations.ipynb] (https://github.com/Ved-Piyush/DeepCropVision_maizegxeprediction2022/blob/main/Data_PreProcessing.ipynb). This script will create the datasets `train_b1.csv`, `test_b1.csv`, `valid_b1.csv`, `train_b1_target.csv`, `test_b1_target.csv`, `valid_b1_target.csv` which correspond to the training set features, testing set features, validation set features, training set targets, testing set targets, and the validation set targets respectively. It will also create the files `trait_cols.csv`,  `meta_cols.csv`, `soil_columns.csv`, `weather_cols.csv`, `EC_cols.csv`, and `hybrid_cols.csv` which have the column names for trait, meta, soil, weather, EC, and hybrid genotype features. 

4. Run the script [Modeling_Script.ipynb](https://github.com/Ved-Piyush/DeepCropVision_maizegxeprediction2022/blob/main/Modeling_Script.ipynb) which will use the files created above to fit the multi-arm dl architecture. Within the script it will also create predictions for the test set which would be included in the pandas dataframe called `sub_file`. 
