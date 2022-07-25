# matplotlib-challenge

## Observations and Insights
1. Ramicane treatment data matches very closely with that of Capomulin
2. Capomulin tretment data shows strong correlation between weight and tumor volume is 0.84, which tells us that the higher the weight the greater the volume of the tumor.
3. The distribution of female or male mice in the study is quite even. i.e 49/51(female/male)

## Background

* A new pharmaceutical company that specializes in anti-cancer pharmaceuticals. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

* The company have the complete [data](Pymaceuticals/data) from their most recent animal study. In this study, 249 mice identified with SCC tumor growth were treated with a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. 

* This [pymaceuticals.ipynb](Pymaceuticals/pymaceuticals.ipynb) will generate all the tables and figures needed for the technical report of the study. It also provide the top-level summary of the study results.

## Instructions

### Prepared the Data

1. Run the provided package dependency and data imports, and then merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.

2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining step. (Note: you found a mouse ID that had duplicate time points, and none of the data associated with that mouse ID should be included in the new DataFrame.)

3. Display the updated number of unique mice IDs.

### Summary Statistics

Two summary statistics DataFrames:

    * Used the `groupby` method to generate the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen. This results in five unique series objects. Which is combine into a single summary statistics DataFrames.

    * The second table, uses the agg method to produce the same summary statistics table by using a single line of code. 

### Create Bar Charts and a Pie Charts

1. Two bar plots. Both plots are identical and show the total number of timepoints for all mice tested for each drug regimen throughout the course of the study.

    * Created the first bar plot by using Pandas's `DataFrame.plot()` method.

    * Created the second bar plot by using Matplotlib's `pyplot` methods.

2. Two pie plots. Both plots are identical and show the distribution of female or male mice in the study.

    * Created the first pie plot by using both Pandas's `DataFrame.plot()`.

    * Created the second pie plot by using Matplotlib's `pyplot` methods.

### Quartiles, Outliers, and a Box Plot 

1. Calculated the final tumor volume of each mouse across four of the most promising treatment regimens: 
    * Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculated the quartiles and IQR and determine if there are any potential outliers across all four treatment regimens. 
   
2. Using Matplotlib, generated a box plot of the final tumor volume for all four treatment regimens. Highlighted any potential outliers in the plot by changing their color and style.
  

### Created a Line Plot and a Scatter Plot

1. For a mouse that was treated with Capomulin. Generated a line plot of tumor volume vs. time point for that mouse.

2. Generated a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

### Calculated Correlation and Regression

1. Calculated the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. 

2. Plotted the linear regression model on top of the previous scatter plot.