IMPORT LIBRARIES
IMPORT ALL NECESSARY LIBRARIES SUCH AS NUMPY, PANDAS, MATPLOTLIB,SEABORN
LOAD DATA
LOAD THE DATASET USING PANDAS (e.g., pd.read_csv('housing_data.csv‘))
DISPLAY FIRST FIVE ROWS
USE df.head() TO VIEW THE FIRST FIVE ROWS OF THE DATASET.
SHAPE OF THE DATA, GET THE SHAPE OF THE DATASET USING df.shape.
DESCRIPTIVE STATISTICS, GET STATISTICAL VALUES OF THE DATA USING df.describe()
FIND NULL VALUES, FIND THE NULL VALUES IN THE DATASET USING df.isnull.sum().
Univariate Analysis (Categorical), Univariate Analysis of Categorical Data,sns.countplot(x='categorical_column', data=df),plt.show(),Explanation: Analyze the distribution of categorical variables using count plots.
Changing Column Values (MSZoning), Changing Values in MSZoning, df['MSZoning'] = df['MSZoning'].replace({'OldName': 'NewName'}), Explanation: Update the values in the MSZoning column with new names.
Univariate Analysis (MSZoning), Univariate Analysis of Categorical Data, sns.countplot(x='MSZoning', data=df), plt.show(), Explanation: Examine the distribution of values in the MSZoning column using count plots.
Replacing Column Values (Shape of Property), Replacing Values in Shape of Property, df['ShapeOfProperty'] = df['ShapeOfProperty'].replace({'OldName': 'NewName'}), Explanation: Change the names in the ShapeOfProperty column.
Univariate Analysis (Shape of Property), Univariate Analysis of Property Shape, sns.countplot(x='ShapeOfProperty', data=df), plt.show(), Explanation: Analyze the distribution of values in the Shape Of Property column
Replacing Column Values (Type of Utilities), Replacing Val
df['TypeOfUtilities'] = df['TypeOfUtilities'].replace({'OldName': 'NewName'}),ues in Type of Utilities, Explanation: Update the names in the TypeOfUtilities column.
Replacing Column Name, Replacing Column Name, df.rename(columns={'OldName': 'NewName'}, inplace=True), Explanation: Change the column name to a more descriptive one
Univariate Analysis, Univariate Analysis, sns.histplot(df['numerical_column'], kde=True), plt.show(), Explanation: Perform univariate analysis of numerical data using histograms.
Bivariate Analysis (Categorical vs Numerical), Bivariate Analysis: Categorical vs Numerical, sns.boxplot(x='categorical_column', y='numerical_column', data=df), plt.show(), sns.boxplot(x='categorical_column', y='numerical_column', data=df), plt.show(), Explanation: Explore the relationship between a categorical and numerical variable using box plots.
Bivariate Analysis (Numerical vs Numerical),Bivariate Analysis: Numerical vs Numerical,sns.scatterplot(x='numerical_column1', y='numerical_column2', data=df), plt.show(), Explanation: Investigate relationships between two numerical variables using scatter plots.
Analyzing Correlation, Analyzing Correlation in a Dataset, correlation_matrix = df.corr(),sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm'),plt.show(), Explanation: Calculate and visualize the correlation matrix to understand variable relationships.
Removing Outliers and Visualization, Removing Outliers and Visualizing Data
# Identify outliers and remove them,
Q1 = df['Value'].quantile(0.25)
Q3 = df['Value'].quantile(0.75)
IQR = Q3 - Q1
df_no_outliers = df[(df['Value'] >= Q1 - 1.5 * IQR) & (df['Value'] <= Q3 + 1.5 * IQR)]

# Plot before and after
plt.figure(figsize=(14, 6))
sns.histplot(df['Value'], kde=True, bins=30, label='Before')
sns.histplot(df_no_outliers['Value'], kde=True, bins=30, label='After', color='red')
plt.legend()
plt.show()
Explanation: Remove outliers and compare visualizations before and after the removal.
Conclusion:- Summary of Key Points:Data loading and inspection
Data cleaning and handling missing values
Univariate and bivariate analysis
Correlation analysis
Outlier removal and its impact
Key Insights:Improved data quality and understanding
Enhanced visualizations
Next Steps:Further analysis or model building
Validation and reporting
