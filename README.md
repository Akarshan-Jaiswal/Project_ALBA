[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/58HShPQN)
# Data Mining and Machine Learning Group Coursework

> [!NOTE]
> You should update and customize this README as the project progresses.

> [!IMPORTANT]
> See the COURSEWORK specification on CANVAS for details of the group coursework criteria/deliverables

## Group Members

> [!IMPORTANT]
> Include your names and `@` your GitHub usernames for each.

1. Akarshan Jaiswal @Akarshan-Jaiswal
2. Jagatheesh Pugazhenthi Pulavan @Jaga-droid
3. Drashti Miteshkumar Shah @drashtishah3334
4. Lahja Ndjalo @Omagano27

## Initial Project Proposal

> The AIM of this project is to help in reducing the overall deprivation in Scotland
> by analyzing the SIMD(Scottish Index of Multiple Deprivation) for Multiple years
> and help in prevention/dispatch of emergency services in the most deprived regions.

### Research objectives

> [!NOTE]
> What are the questions you are trying to answer? What are the goals of your project?

### Milestones

> [!NOTE]
> Create a bullet list of the key milestones for your project. Discuss these with your group. You may need to update these as the project progresses.

    Milestone 1(18th Sep-24th Sep): Project Topic, Direction, and Questions.
    Milestone 2(25th Sep-8th Oct): Data Analysis and Exploration.
    Milestone 3(9th Oct-22nd Oct): Clustering.
    Milestone 4(23rd Oct-10th Nov): Decision Trees.
    Milestone 5(11th Nov-27th Nov): Convolutional Neural Networks.


## Findings Report

<!-- Below you should report all of your findings in each section. You can fill this out as the project progresses. -->

### Research objectives
> [!NOTE]
> What are the most prominent contributing factors to the overall Deprevation existing in Scotland?
> Which regions are the most deprived according to the dataset?
> Where in these regions are the most emergency/social services needed?

### Datasets
1. SIMD(Scottish Index of Multiple Deprivation) for the years 2016 and 2020
   - [SIMD_2016_Data](data/SIMD_2016_Data.xlsx)
   - [SIMD_2020_Data](data/SIMD_2020_Data.csv)
2. Cleaned, preprocessed and final combined dataset that we used
   - [combined_dataset](data/processed_data/combined_dataset.csv)   
#### Dataset description
<!-- Briefly describe your task and dataset -->
   - The Scottish Index of Multiple Deprivation is a relative measure of deprivation across 6,976 small areas (called data zones).
   - If an area is identified as ‘deprived’, this can relate to people having a low income but it can also mean fewer resources or opportunities.
   - SIMD looks at the extent to which an area is deprived across seven domains: income, employment, education, health, access to services, crime and housing.
   - SIMD is the Scottish Government's standard approach to identify areas of multiple deprivation in Scotland.
   - It can help improve understanding about the outcomes and circumstances of people living in the most deprived areas in Scotland.
   - It can also allow effective targeting of policies and funding where the aim is to wholly or partly tackle or take account of area concentrations of multiple deprivation.
   - SIMD ranks data zones from most deprived (ranked 1) to least deprived (ranked 6,976).
   - The Scottish Index of Multiple Deprivation 2020 has been revised as a result of a problem identified with the income domain ranks provided by the Department for Work and Pensions.
   - This revision only affects the income domain ranks and overall SIMD ranks.
   - Below file describe the Dataset Indicators:
        - [SIMD_2016_Indicator_descriptions](data/SIMD_2016_Indicator_descriptions.xlsx)

#### Dataset examples
<!-- Add a couple of example instances and the dataset format -->

#### Dataset exploration
<!-- What is the size of the dataset? -->
   - After Cleaning and Preprocessing the dataset the size of the [Combined Dataset](data/processed_data/combined_dataset.csv) is 8042.
<!-- Train,validation,splits? -->
   - We did Validation split of 80:20 in CNN.
   - Similarly we did a combination of [60:20:20] and [80:20] split of data in decision trees. 
<!-- Summary statistics of your dataset -->
|       |   Unnamed: 0 |   Total_population |   Working_age_population_revised |   Income_rate |   Income_count |   Employment_rate |   Employment_count |   ALCOHOL |      DRUG |       SMR |     EMERG |    Noquals |         NEET |   drive_petrol |    drive_GP |    drive_PO |   drive_primary |   drive_retail |   drive_secondary |      PT_GP |    PT_Post |   PT_retail |   overcrowded_count |   nocentralheat_count |   overcrowded_rate |   nocentralheat_rate |       year |
|:------|-------------:|-------------------:|---------------------------------:|--------------:|---------------:|------------------:|-------------------:|----------:|----------:|----------:|----------:|-----------:|-------------:|---------------:|------------:|------------:|----------------:|---------------:|------------------:|-----------:|-----------:|------------:|--------------------:|----------------------:|-------------------:|---------------------:|-----------:|
| count |      8042    |           8042     |                         8042     |  8040         |      8042      |      8040         |          8042      | 8042      | 8042      | 8042      | 8042      | 8042       | 8039         |    8042        | 8042        | 8042        |     8042        |    8042        |        8042       | 8042       | 8042       |  8042       |           8042      |             8042      |       8042         |        8042          | 8042       |
| mean  |      4020.5  |            773.621 |                          500.776 |     0.121623  |        92.6556 |         0.105061  |            51.3819 |   99.3302 |   95.9473 |   98.9903 |   99.0078 |   99.5894  |    0.0640142 |       3.66479  |    3.34781  |    2.72708  |        2.56973  |       5.08169  |           5.94542 |   10.0461  |    8.46987 |    13.1028  |             83.8701 |               13.7666 |          0.11132   |           0.018261   | 2016.53    |
| std   |      2321.67 |            200.509 |                          163.737 |     0.0954243 |        75.2616 |         0.0797297 |            41.2386 |   99.7902 |  147.091  |   45.6776 |   34.1483 |   55.6031  |    0.0611729 |       2.78876  |    2.64708  |    1.56451  |        3.21359  |       5.76508  |           4.89682 |    5.94259 |    4.38644 |    10.1271  |             65.1283 |               17.7837 |          0.0799606 |           0.0225269  |    1.35645 |
| min   |         0    |              0     |                            0     |     0         |         0      |         0         |             0      |    0      |    0      |    0      |   19.7177 |    2.99499 |    0         |       0.619681 |    0.558916 |    0.594656 |        0.687859 |       0.685475 |           1.01779 |    1.60127 |    1.93057 |     1.83543 |              0      |                0      |          0         |           0          | 2016       |
| 25%   |      2010.25 |            638     |                          400     |     0.05      |        35      |         0.04      |            20      |   32.7992 |    0      |   70      |   72.6558 |   55.044   |    0.02      |       2.18361  |    1.92711  |    1.73708  |        1.66303  |       2.7775   |           3.62899 |    6.26757 |    5.56898 |     7.82384 |             36      |                3      |          0.05      |           0.00428342 | 2016       |
| 50%   |      4020.5  |            758     |                          479     |     0.1       |        70      |         0.08      |            40      |   70.1659 |   43.3202 |   92      |   93.0656 |   90.3793  |    0.05      |       2.98824  |    2.73659  |    2.38418  |        2.21306  |       3.94624  |           4.77694 |    8.66551 |    7.46504 |    10.9692  |             68      |                8      |          0.09375   |           0.0103448  | 2016       |
| 75%   |      6030.75 |            884     |                          569     |     0.18      |       130      |         0.15      |            70      |  133.146  |  129.245  |  120      |  120.54   |  138.233   |    0.09      |       4.11098  |    3.88916  |    3.23008  |        2.95388  |       5.73035  |           6.5313  |   12.0073  |   10.1398  |    15.4992  |            114      |               17      |          0.152297  |           0.0235103  | 2016       |
| max   |      8041    |           3847     |                         3423     |     0.73      |       555      |         0.53      |           325      | 2350.54   | 1864.13   |  950      |  323.786  |  353.078   |    0.5       |      63.5065   |   87.8162   |   17.3199   |      186.132    |     190        |         116.149   |  108.79    |   40.2779  |   190       |            490      |              187      |          0.583882  |           0.214964   | 2020       |
<!-- Visualisations of your dataset -->
<!-- Analysis of your dataset -->
   - Column comparision of 2016 and 2020 files: [Column Comparision](data/2016_2020_DataColumn_Comparison_27092023.xlsx)
   - Notebook containing code for the following exploratory analysis.

        - Consolidated EDA Notebook:- [EDA_Notebook](notebooks/EDA_Notebook.ipynb)

   - Archived Notebooks containing code for the following exploratory analysis.

        - Dtale:- [PrimaryEDA_Script](notebooks/PrimaryEDA_Script.ipynb)

        - Sweetviz:- [SIMD_2020_EDA_Jagatheesh](notebooks/SIMD_2020_EDA_Jagatheesh.ipynb)

        - Autoviz:- [EDA_DTale_AutoViz_Drashti](notebooks/EDA_DTale_AutoViz_Drashti.ipynb)
   
   - These areas are the worst affected areas
      - East Ayrshire
      - North Ayrshire
      - Inverclyde
      - Dundee City
      - Fife

### Clustering
   - Notebook containing Implemented various clustering algorithms on the dataset:
      - Consolidated Clustering Notebook:- [Clustering_Notebook](notebooks/Clustering_Notebook.ipynb)
   
   - Archived Implemented various clustering algorithms on the dataset:
      - [1. K-Means](notebooks/Kmeans_clustering.ipynb)
      - [2. BIRCH(Balanced iterative reducing and clustering using hierarchies) Clustering](notebooks/BIRCH_Clustering.ipynb)
      - [3. Affinity Propagation Clustering](notebooks/Clustering_Scripts.ipynb)
      - [4. DBSCAN Clustering](notebooks/DBSCAN_Clustering_Output.ipynb)
	   - [5. OPTICS Clustering](notebooks/OPTICS_Clustering.ipynb)
	   - [6. Gaussian Clustering](notebooks/Clustering_Scripts.ipynb)
	   - [7. K-medoid Clustering](notebooks/KMediod_Cluster.ipynb)

#### Experimental design
<!-- Describe your experimental design and choices for the week. -->

#### Results
<!-- Tables showing the results of your experiments -->

#### Discussion
<!-- A brief discussion on the results of your experiment -->

### Decision Trees

#### Experimental design
<!-- Describe your experimental design and choices for the week. -->
 We decided to consider the following features as our target variable: 
    1. Employment_count
    2. Substance_Abuse 
1.Employment_count : 
- Employment_count had positive correlations with a good number of features in our combined SIMD dataset. We wanted to find which features influenced the number of employed people across the regions in Scotland. 
- We utilized binning to convert our Employment_count to a categorical variable and applied
decision trees, used feature selection and pruning to improve the model.


   

#### Results

1. Employment_count : 
|               | Precision |   Recall | F1-Score |   Support |
|:--------------|----------:|---------:|---------:|----------:|
| 0             |   0.96524 | 0.976884 | 0.971029 |       995 |
| 1             |   0.93153 | 0.885602 | 0.907988 |       507 |
| 2             |   0.80672 | 0.905660 | 0.853333 |       106 |
| Accuracy      |   0.94341 | 0.943408 | 0.943408 |   0.94341 |
| Macro Avg     |   0.90117 | 0.922715 | 0.910783 |      1608 |
| Weighted Avg  |   0.94416 | 0.943408 | 0.943394 |      1608 |



<!-- Tables showing the results of your experiments -->

#### Discussion
<!-- A brief discussion on the results of your experiment -->
1. Employment_count:
- First, a base model was built with all features. Then, Recursive feature elimination was used to trim the dataset to help optimize predictions. After checking that variance error was high which can lead to overfitting, pruning was performed to help reduce it. This led to a slight decrease in variance error and a reasonable increase in model accuracy. It was observed that these features contributed the most to predicting the Employment_count:
    - Data_Zone	
	 - nocentralheat_rate	
	 - drive_secondary	
	 - PT_GP	
	 - crime_rate	
	 - DRUG	
	 - NEET	
    - CIF	
	 - ALCOHOL	


### Neural Networks

#### Experimental design
<!-- Describe your experimental design and choices for the week. -->

#### Results

<!-- Tables showing the results of your experiments -->

#### Discussion
<!-- A brief discussion on the results of your experiment -->


### Conclusion
<!-- Final conclusions regarding your initial objectives -->
