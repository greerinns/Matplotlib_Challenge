# Matplotlib Sample

## Dependencies
- Import the necessary dependencies, including matplotlib, pandas, scipy, and numpy.

## Reading in Data
- Create filepaths to access the data files.
- Read in the CSV data using the pandas function.
- Examine the first few rows of the data using the `.head()` function to display a preview.

## Merging and Unique IDs
- Merge DataFrames on the "Mouse ID" column.
- Use a pandas function to determine the number of unique "Mouse ID" values.
- Sort the DataFrame by "Mouse ID" and "Timepoint" in ascending order.
- Use the `duplicated` function to identify duplicate "Mouse ID" values and retrieve their indexes.
- Use the `loc` function to display the rows with duplicate "Mouse ID" values.
- Remove the duplicate "Mouse ID" using the `loc` function.
- Display the new unique values in the "Mouse ID" column.

## Drug Regimen
### Regimen Stats
- Group the DataFrame by "Drug Regimen."
- Use the `agg` function to calculate summary statistics for each regimen.

### Regimen Timepoints
- Group the DataFrame by "Drug Regimen" again, using the `agg` function to count the number of timepoints for each regimen.
- Use pandas and matplotlib to create a bar graph showing the number of timepoints for each drug regimen.

## Male vs. Female
- Extract the "Sex" column from the unique DataFrame.
- Use the `value_counts` function to count the occurrences of each gender.
- Create a pie chart using matplotlib and pandas to visualize the gender distribution.

## Calculate Quartiles, Find Outliers, and Create a Box Plot
- Group the mice by "Mouse ID" and select the maximum timepoint for each mouse.
- Merge this data back into the unique DataFrame using an inner join to keep only the final tumor volume data.
- Create a list to store tumor volume data for the four specific treatment names: 'Capomulin', 'Ramicane', 'Infubinol', and 'Ceftamin'.
- Append all final tumor volumes for each treatment to the list.
- Calculate potential outliers using the upper and lower bounds (1.5 times the interquartile range) for each treatment.
- Create a box plot for the final tumor volumes, highlighting any potential outliers in red.

## Capomulin
- Narrow down the unique DataFrame to include only subjects treated with Capomulin.
- Select the first mouse treated with Capomulin and create a line plot of "Tumor Volume" vs. "Timepoint."
- For the entire Capomulin subset, group the data by "Mouse ID" and use the `agg` function to calculate the mean of "Tumor Volume" and the weight of the mice.
- Create a scatter plot of average tumor volume vs. weight for mice treated with Capomulin.

## Linear Regression
- Use the `scipy` library's `linregress` function to calculate the correlation coefficient (r), slope (m), and y-intercept (b).
- Create a linear regression line using the formula y = mx + b.
- Plot the linear regression line over the scatter plot from the Capomulin section to visualize the relationship between tumor volume and weight.
