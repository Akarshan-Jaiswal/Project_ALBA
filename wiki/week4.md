# Week 4

## Tasks
- [X] Formulating research objectives for the project.

- [X]  Further Data Cleaning Steps including rectifying errors in data entries and taking care of sparse rows.
    - Analysing both the data files of year 2016 and 2020.
    - Cleaned the `data/simd2020 (1).csv` ([group-coursework-valhalla/notebooks/Data_Cleaning_simd_2020.ipynb](group-coursework-valhalla/notebooks/Data_Cleaning_simd_2020.ipynb)) to generate a clean dataset for year 2020 (`data/cleaned_2020.xlsx`).
		- Checked if the "id" column has value of "geom" column, then shifted all the columns to right.
    - Created pipeline ([group-coursework-valhalla/notebooks/preprocessed_combined_dataset.ipynb](group-coursework-valhalla/notebooks/preprocessed_combined_dataset.ipynb)) to combine the dataset (`data/combined_dataset.csv`).
		- Created dataframes of both the files.
		- Dropping unnecessary columns from SIMD 2020 dataframe.
		- Creating Data Dictionary for mapping header names.
		- Renamed headers in SIMD 2020 dataframe.
		- Added column "year" in both 2016 and 2020 dataframes.
		- Combined both the dataframes.

- [X] Initiated application of clustering algorithms on the dataset.
	- Started working on various Clustering Algorithms: BIRCH Clustering, DBSCAN Clustering, OPTICS Clustering, Gaussian Clustering, Affinity Clustering, K-Means Clustering and KMedoid Clustering with sample data to understand how it works, later implementing it for actual dataset.
