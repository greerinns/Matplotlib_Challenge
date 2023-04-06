# Matplotlib_Challenge
## Dependencies
- Import dependencies
- Using matplotlib, pandas, scipy, and numpy
## Reading in data
- Create filepaths
- Read in CSV using pandas function
- Examine with .head() displays
## Merging and Unique IDs
- Merge DFs on Mouse ID
- Use pandas function to get number of unique IDs
- Sort by ID and timepoint
- Use duplicated function to get duplicate IDs and grab indexes
- Use loc to display duplicate rows
- Drop duplicate ID using loc function
- Show new unique values
## Drug Regimen
### Regimen Stats
- Group by drug regimen
- Use agg function to gather summary stats
### Regimen Timepoints
- Group by drug regimen again using agg function to count timepoints for each
- Use pandas and matplotlib to plot bar graph of Timepoints for each drug regimen
## Male vs Female
- Grab 'Sex' column of unique dataframe
- Use value counts function to total each type
- Plot as pie in matplotlib and pandas
## Calculate Quartiles, Find Outliers, and Create a Box Plot
- Group mice by ID with max timepoint
- Merge back to unique DF using inner join to keep only final tumor volume
- Using a list to store tumor volume lists, index through the dataframe by treatment name: 'Capomulin', 'Ramicane', 'Infubinol', and 'Ceftamin'
- Append all final tumor volumes for each treatment
- Calculate outliers using above 3rd quartile by 1.5 x IQR and below the first by 1.5 x IQR (IQR by subtracting 3rd q by 1st q)
- Plot as a box plot, marking the outlier in red
## Capomulin
- Narrow unique dataframe down to Capomulin subjects
- Grab the first mouse treated with Capomulin, and plot Tumor Vol vs Time
- Going to the whole Capomulin subset, groupby Mouse ID and agg Tumor Volume as mean and Weight as itself
- Plot Average Tumor Volume by weight
## Linear Regression
- Use scipy linregress to determine r, m, and b
- Create linear regression line as y = m(weight) + b
- Plot linear regression over plot from Capomulin section
