# Analyze Supermarket Data Across the Country - Company XYZ
Company XYZ owns a supermarket chain across the country. Each major branch located in 3 cities across the country recorded sales information for 3 months, to help the company understand sales trends and determine its growth, as the rise of supermarkets competition is seen.

You will apply learnings to analyse the dataset in the data folder, and the description of each feature can be found in this link
To-Do - Write a short project description here.
[Here is the complete analysis](https://github.com/Tiamiyu1/Data-Analysis-Project/blob/main/Super%20Market%20%20Data%20Analysis_Updated.ipynb)
# Project Steps
## Step 1 - Loading the Dataset
The dataset consists of 3 separate csv files of each branch, the 3 files were put into a list(having same .csv extension) using os module and glob modules.
Individual file in the list is read and concatenated into a single csv file with pd.read_csv.
The combined file was exported to a csv file using .to_csv  and was read back into a dataframe named data using pd.read_csv for analysis

## Step 2 - Data Exploration
Imported necessary libraries:
- numpy and pandas for dataframe manipulation
- matplotlib and seaborn for data 

Checked the head() to see how the first few rows look like
Shape attribute tells us that the combined data has 1000 rows with 17 features each
data.columns gives a list of the column names
Decsribe shows brief deccription of the dataset like; count, mean, std, min, max, 25, 50 and 75 percentile. Extreme values can be spotted here

Observation
- Minimun and maximum rating is 4 and 10 respectively
- Tax and gross income look statistically alike

.info() gives quick information about the whole dataset such as data type, missing values, number of columns and rows


## Step 3 - Dealing with DateTime Features
The date and time columns were changed to datetime data type which made it easy to extract day, year, month, hour of transactions
All transaction occurs in 11 out of the 24hrs in a day, from 10am till 8pm


## Step 4 - Unique Values in Columns
unique() and nunique() methods show the distinct entities and the number of disctinct entities in a particular column respectively
The branch column has 3 unique values, city has 3, customer type has 2, gender has 2, product line has 6, payment has 3


## Step 5 - Aggregration with GroupBy
Groupby function makes grouping by column easy
Aggregate functions such as min, max, mean, sum can be performed on the groupby object to better understand the data

## Step 6 - Data Visualization
Visualization shows graphical representation of different columns in the dataset
Countplot shows distribution of a categorical variable




# Insights

- Minimun and maximum rating is 4 and 10 respectively
- Tax and gross income look statistically alike
- Port Harcourt has the highest total gross income, reason for its highest tax
- Lagos has the highest total unit price, quantity and rating
- Port Harcourt paid the highest tax while Lagos paid the least
- Branch A (Lagos) has the highes sales record
- Epay is the payment mostly used across the 3 locations
- Fashion accessories is the most purchased product across the 3 locations,  Health and beauty is the least
- People that purchase Electronic accessories pay mostly in cash
- Epay is mostly used in Lagos, card in Abuja and cash in Port Harcourt
- Branch B (Abuja) has the lowest total rating
- On average, Females buy more of Fashion accessories & Home and lifestyle than males
- Also, males buy more of Health and beauty
- The other three product lines (ood and beverages, sports and travel & Electronic accessories) appear equally distributed among the two genders


- Females spend more on Food and beverages , Fashion accessories & Home and lifestyle than males
- Males spend more on Health and beauty  & sports and travel than females
- Seems both gender spend equally on Electronic accessories  
- Electronics has the lowest unit price while fashion accessories has the highest unit price
- Electronics has the highest quantity purchased (probably due to its lowest unit price) while fashion accessories has the lowest quantity purchased (opposite reason)

# Future Work
Predictive analysis:
Given a dataset for previous years, coming year gross income (profit) can be predicted for each location

# Standout Section
More Insights:
- Most customers in Port Harcourt are females
- The two customer types are equally distributed
- All transactions occured within 3 months with most sales record in January, followed by march then February

I make sure the legend doesn't overlap the plot
I change the extension to Branch.csv to avoid adding the combined csv file when running the code over and over again

# Executive Summary.
I tried to explain each line of code as comment and markdwon in this notebook

Further documentation can be found in the read.me of this git repo
