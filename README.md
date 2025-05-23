# EMATMOO48-Part 2: Earthquake Analysis Project

- The goal of this project is to analyze earthquake data from throughout the world from 2013 to 2023 in order to determine 
the features of earthquake events and the factors that affect tsunami alerts. The USGS Earthquake API provided the data, 
which was then examined using Python modules and a Jupyter Notebook. 

## Data Gatering

- URL: https://earthquake.usgs.gov/ 
- Data Source: USGS Earthquake API

### Procedure for Data Retrieval:
		
- To retrieve data by using the API, use the requests library.
- Indicate the parameters, including start_time and end_time, which is the range of times for data collecting
  and min_magnitude is earthquake minimum magnitude.
- Use pandas to transform the API response into a structured DataFrame.
- To facilitate additional analysis, save the extracted data as a CSV file.


### The dataset's variables include:
	
- time: The time when this earthquake occurred.
- magnitude: The size of earthquake.
- depth: The earthquake's depth (in kilometers).
- the geographic coordinates are latitude and longitude.
- tsunami_alert: A tsunami alert indicator (0 = no alert, 1 = alert).
	
 ### Data Management:

- To get around API restrictions, extract data in annual chunks (chunking).
- Integrate all of the data.
- Create a file called earthquake_raw_data.csv and save the entire dataset.


## Data Analysis
	
### Key Questions:

- What characteristic of earthquake have an impact on tsunami alert?
- Does the depth of an earthquake influence tsunami alerts?
- How does higher magnitude correlate with tsunami alerts?
- Is there a relationship between depth and magnitude?
- How are tsunami alerts distributed across depth categories?
- What are the correlations between magnitude, depth, and tsunami alerts?
- How do magnitude and depth distributions differ for earthquakes that 
trigger tsunami alerts versus those that do not?
- What are the characteristics of shallow earthquakes?

### Steps in Analysis:
		
- Determine the mean, maximum, and minimum values for basic statistics.
- Examine how variables such as tsunami alerts, depth, and magnitude are distributed.
- To depict relationships, use a variety of plots, such as box plots, bar charts, and scatter plots.
- Look for relationships between characteristics like magnitude and depth.

### Results:

- Tsunami alerts have a possibility in shallow earthquakes (less than 70 km) with 
magnitudes greater than 5.5. It is evident that tsunami warnings are influenced by magnitude. 
There is no significant correlation between depth and magnitude.

### Libraries 
	
- Python Libraries:
		
- requests:
	- Use it to send HTTP requests to APIs in order to retrieve data. Features include 
	handling HTTP methods such as POST and GET and parsing JSON replies from APIs is handled by 
	this function.

- Pandas:
	- It manages the storage, processing, and transformation of the seismic dataset in the DataFrame 
	and serves as a tool for data manipulation and analysis. Features include the ability to import and 
	export data in CSV, JSON, and other formats. It offers statistical analysis, filtering, and grouping 
	functions. Additionally, working with other machine learning and visualization packages.

- Seaborn and matplotlib: 
	- The goal of both libraries is to visualize data. Matplotlib can offer common tools 
	for making common plots, like line charts, bar plots, and scatter plots, while Seaborn is capable 
	of producing statistical plots with eye-catching default themes, such as boxplots and pair plots.

- Numpy:
	- This is used to compute numerical values and carry out operations on arrays and numerical data, 
	like mathematical transformations or statistical computations. Its features including, using its array object 
	to manage big datasets and provides a large range of mathematical functions, including standard deviation, 
	mean, and median.
		
- The chi-square test, or scipy: 
	- The goal is to assess the correlations between variables by doing statistical tests. Its features 
	are accommodates independence tests using chi-square and it good for determining the importance 
	of correlations in contingency tables, like tsunami warnings vs magnitude criteria.
	
- Command to Install Libraries pip install requests pandas matplotlib seaborn numpy scipy



## How to Run the Code

- Download the project files or clone the repository.
- Open the terminal and navigate to the project folder: cd ~/project
- Launch Jupyter Notebook: jupyter notebook
- Install libraries and run the cells sequentially.
- Review the outputs and visualizations in the Notebook.

> [!TIP]
> Missing Libraries: If an error occurs because of a missing library, re-run the installation command:
> -pip install requests pandas matplotlib seaborn numpy scipy
> API Errors:
> - Makes sure an active internet connection to fetch data from the API.
> - If the API server is down, try again later or verify the API URL.


## File Structure
- project.ipynb: Jupyter Notebook containing the code and analysis.
- earthquake_raw_data.csv: The dataset extracted from the API.
- earthquake_df_cody.csv: The cleaned data.
- readme.md: Documentation explaining the project.
