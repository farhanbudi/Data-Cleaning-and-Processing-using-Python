# Data Cleaning and Data Processing Using Python

In this project, I created a python project using pandas and matplotlib library. the purpose of this project is to clean up the data, combine data from 3 different sources, and perform data analysis and data processing of the cleaned data.

There are 3 datasets used in this project:

1. List of indicators of energy supply and renewable electricity production from the United Nations for the year 2013. This data has xls format and has 7 columns and 283 rows. This data has the file name `Energy Indicators.xls`, and the source of this dataset is [here](http://unstats.un.org/unsd/environment/excel_file_tables/2013/Energy%20Indicators.xls). 
2. GDP data from a country from 1960 to 2015 from World Bank. This data has csv format and has 60 columns and 269 rows. This data has the file name `world_bank.csv`, and the source of this dataset is [here](http://data.worldbank.org/indicator/NY.GDP.MKTP.CD). 
3. Sciamgo Journal and Country Rank data for Energy Engineering and Power Technology, which ranks countries based on their journal contributions in the aforementioned area. This data has xlsx format and has 8 columns and 192 rows. This data has the file name `scimagojr-3.xlsx`, and the source of this dataset is [here](http://www.scima-gojr.com/countryrank.php?category=2102).

## Data Cleaning

First, we do data cleaning on the three data. Data cleaning performed on data `Energy Indicators.xls`:
-	Exclude the header and footer information from the datafile and delete other unnecessary data.
-	Convert Energy Supply from petajules to gigajoules.
-	Change missing data ("…") to NaN values.
-	Remove numbers and/or parenthesis from several countries in their name.
-	Rename some countries to match other data:
    -   "Republic of Korea": "South Korea",
    -	"United States of America": "United States",
    -	"United Kingdom of Great Britain and Northern Ireland": "United Kingdom",
    -	"China, Hong Kong Special Administrative Region": "Hong Kong".

Data cleaning performed on data `world_bank.csv`:
-	Exclude the header from the datafile and delete other unnecessary data.
-	Remove column Country Code, Indicator Name, and Indicator Code.
-	Only use data from 2016 – 2015.
-	Rename some countries to match other data:
    -	"Korea, Rep.": "South Korea", 
    -	"Iran, Islamic Rep.": "Iran",
    -	"Hong Kong SAR, China": "Hong Kong".

No data cleaning performed on data `scimagojr-3.xlsx`. Then, join the three datasets: Energy Indicators, GDP, and Scimagojr. Only use data from top 15 Scimagojr "Rank".

## Data Processing

1. What is the average GDP over the last 10 years for each country?
2. From the country with the 6th largest average GDP, how much had the GDP changed over the 10 years?
3. What country has the maximum % Renewable and what is the percentage?
4. Create a new column that is the ratio of Self-Citations to Total Citations. What is the maximum value for this new column, and what country has the highest ratio?
5. Create a column that estimates the population using Energy Supply and Energy Supply per capita. What is the third most populous country according to this estimate?
6. Create a column that estimates the number of citable documents per person (Population Estimation, as previously calculated). What is the correlation between the number of citable documents per capita and the energy supply per capita?
7. Show the correlation plot in Top15!
8. Use the following dictionary to group the Countries by Continent, then create a dataframe that displays the sample size (the number of countries in each continent bin), and the sum, mean, and std deviation for the estimated population of each country.
9. Cut % Renewable into 5 bins. Group Top15 by the Continent, as well as these new % Renewable bins. How many countries are in each of these groups?

For the results of data processing, and portfolio for this project in pdf can be accessed [here](https://drive.google.com/drive/folders/1492zZHvWoXR5gUkLeoM3ZCWhkYJl4z8y?usp=sharing).
