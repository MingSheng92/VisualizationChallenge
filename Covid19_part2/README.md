# Covid 19 visualization Part 2

### Data Source 
The data used in this visualization can be found at [COVID-19 Data Repository](https://github.com/CSSEGISandData/COVID-19)

### Tool
[Power Bi](https://powerbi.microsoft.com/en-us/) 
Python <br />
Jupyter <br />

### Visuzlization
1st draft:

![Figure1](https://github.com/MingSheng92/VisualizationChallenge/blob/main/image/Dashboard.JPG)

Refined version:<br />
This is the latest version where all the calculation is fixed and refined layout.<br />
![Figure2](https://github.com/MingSheng92/VisualizationChallenge/blob/main/image/Dashboard_refined.JPG)

Found a bug in previous code in calculating daily new cases, rewrites calculation logic to fix the error: <br />
With vectoriztion, we improved code execution time and fixed the calculation error. <br />

### Steps taken: 
1. By ETL standard, we will first need to extract the data, as mentioned before then data is collected from [COVID-19 Data Repository](https://github.com/CSSEGISandData/COVID-19) which is widely used by Google, facebook hence this can be treated as a trusted source.
2. Once data is collected, we will use python to clean and process the data obtained, remove any rows that has missing information on geolocation and calculate the daily death, daily new cases and daily recovered cases by using pandas and numpy operations, then save as new csv files.
3. Load onto PowerBI, unpivot the dates column, next append all 3 files (confirmed_case, confirmed_death, and confirmed_recovered) so that it is mergred into one files, added one new coulmn status so that it can be selected with queries.
4. Visualize the data as above.

### future work
1. Heat map adjustment, as for now the heatmap presentation is barely visible ( not sure if there is any possible way to improve it maybe by using scaler)
2. adding machine learning into the visualiztion, by training a regression model we can predict the future cases (with R or python) linear regression or neural network such as LSTM for more advanced predictive model.
3. more graphs, now that we have a base that has scracthed the surface, we can add more meaningful graphs to represent our data to answer our questions 
4. As we always required to download and clean the data before any visualization in PowerBI, it would be really nice to set up a way to automate the steps, Kafka and python should be the way to go if we need to setup a automation pipeline.

### Conclusion 
We have successfully created a visualization to showcase how to Extract, Transform and Load data, from there we learn how fast the virus can spread across countries. 

Stay safe everyone!
