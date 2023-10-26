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
    Milestone 3(9th Oct-22nd Oct): Clustering
    Milestone 4(23rd Oct-): Decision Trees


## Findings Report

<!-- Below you should report all of your findings in each section. You can fill this out as the project progresses. -->

### Research objectives
<!-- What questions you are trying to answer? -->

### Datasets
1. SIMD(Scottish Index of Multiple Deprivation) for the years 2016 and 2020
   - [SIMD_2016_Data](../data/SIMD_2016_Data.xlsx)
   - [SIMD_2020_Data](../data/SIMD_2020_Data.csv)
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
        - [SIMD_2016_Indicator_descriptions](../data/SIMD_2016_Indicator_descriptions.xlsx)

#### Dataset examples
<!-- Add a couple of example instances and the dataset format -->

#### Dataset exploration
<!-- What is the size of the dataset? -->
   - After Cleaning and Preprocessing the dataset the size of the [Combined Dataset](../data/combined_dataset.csv) is 8042.
<!-- Train,validation,splits? -->
<!-- Summary statistics of your dataset -->
<!-- Visualisations of your dataset -->
<!-- Analysis of your dataset -->
   - Column comparision of 2016 and 2020 files: [Column Comparision](../data/2016_2020_DataColumn_Comparison_27092023.xlsx)
   - Notebooks containg code for the following exploratory analysis.

        - Dtale:- [PrimaryEDA_Script](../notebooks/PrimaryEDA_Script.ipynb)

        - Sweetviz:- [SIMD_2020_EDA_Jagatheesh](../notebooks/SIMD_2020_EDA_Jagatheesh.ipynb)

        - Autoviz:- [EDA_DTale_AutoViz_Drashti](../notebooks/EDA_DTale_AutoViz_Drashti.ipynb)

### Clustering
  -  Implemented various clustering algorithms on the dataset:
	
	    - [1. K-Means](../notebooks/Kmeans_clustering.ipynb)
        - [2. BIRCH(Balanced iterative reducing and clustering using hierarchies) Clustering](../notebooks/BIRCH_Clustering.ipynb)
        - [3. Affinity Propagation Clustering](../notebooks/Clustering_Scripts.ipynb)
        - [4. DBSCAN Clustering](../notebooks/DBSCAN_Clustering_Output.ipynb)
	    - [5. OPTICS Clustering](../notebooks/OPTICS_Clustering.ipynb)
	    - [6. Gaussian Clustering](../notebooks/Clustering_Scripts.ipynb)
	    - [7. K-medoid Clustering](../notebooks/KMediod_Cluster.ipynb)

#### Experimental design
<!-- Describe your experimental design and choices for the week. -->

#### Results
<!-- Tables showing the results of your experiments -->

#### Discussion
<!-- A brief discussion on the results of your experiment -->

### Decision Trees

#### Experimental design
<!-- Describe your experimental design and choices for the week. -->

#### Results

<!-- Tables showing the results of your experiments -->

#### Discussion
<!-- A brief discussion on the results of your experiment -->

### Neural Networks

#### Experimental design
<!-- Describe your experimental design and choices for the week. -->

#### Results

<!-- Tables showing the results of your experiments -->

#### Discussion
<!-- A brief discussion on the results of your experiment -->


### Conclusion
<!-- Final conclusions regarding your initial objectives -->
