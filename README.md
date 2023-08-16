# us-medical-insurance-costs
This Python script analyzes an insurance dataset. It explores charges based on smoker status and region, detects potential outliers, and examines relationships between BMI, gender, and charges. Visualizations like box plots and scatter plots provide insights into data patterns. The project aims to understand factors affecting insurance charges.

Data Loading and Overview:

Imports necessary libraries (pandas, matplotlib.pyplot, seaborn).
Loads the "insurance.csv" dataset into a DataFrame (df).
Prints the first few rows of the DataFrame and its basic info using print(df.head()) and print(df.info()).

Summary Statistics:

Prints summary statistics of numeric columns using print(df.describe()).
Distribution of Charges:

Creates box plots to visualize the distribution of charges based on smoker status and region using sns.boxplot().
Displays the distribution of charges based on smoker status and region using plt.show().
Outlier Detection:

Creates box plots to visualize potential outliers in the "charges" and "age" columns using sns.boxplot().
Calculating and Identifying Potential Outliers:

Calculates the Interquartile Range (IQR) for the "charges" column and defines upper and lower bounds for potential outliers.
Identifies potential outliers in the "charges" column using outliers = df[(df['charges'] < lower_bound) | (df['charges'] > upper_bound)].
Prints the potential outliers' age and charges using print(outliers[['age', 'charges']]).
Further Analysis Based on Smoker Status:

Creates a box plot to compare charges based on smoker status using sns.boxplot().
BMI vs Charges Analysis:

Creates a scatter plot to visualize the relationship between BMI and charges using sns.scatterplot().
Gender vs Charges Analysis:

Creates a box plot to compare charges based on gender using sns.boxplot().
Smoking Status by Gender Analysis:

Creates a count plot to visualize the distribution of smoking status by gender using sns.countplot().
Adds a legend to indicate "Non-Smoker" and "Smoker" categories.
BMI by Gender Analysis:

Creates box plots to compare BMI based on gender using sns.boxplot().
