# Project-2-AirMadBcn

## Data
 In this project we gathered information regarding air quality from the collective effort of https://aqicn.org/data-platform/covid19/es/ to pull data from cities all over the word into one document. We downloaded the avaliable data files for 2020, 2019 and 2018 in csv format. Subsequently, we filtered these files with awk, to avoid loading files in GitHub that surpassed the limit of its free version (over 120Mb), and kept only the records for Barcelona and Madrid.

## Methods

We opened the files as a pandas dataframe (df), and created separate df for both cities, and filtered out the weather conditions.
We changed the date column from object to datetime64 type, so month information can be extracted automatically.
After the date conversion, we could use "grupby" to select the pollutants or "Specie" and the different months.
After the groupby, we had to reset the index and we could finally use pivot, to shift the values in the column "Specie" to a new column for each.
We finally obtained a table with the monthly mean of the maximum values recorded daily for every pollutant

## how to use:

Download the python jupyter notebook file.
Open it with jupyter notebook and run all the cells to get the six tables (Madrid and Barcelona for 2020, 2019 and 2018)
,both as csv files and printed in the notebook.