# DietChallenge
In this project I scrape data from cronometer.com and analyze it. From April 1st 2021 to August 14th 2021 I tracked everything I ate, my daily weight, and my exercise on cronometer. I always wondered what I could learn if I could scrape that data and analyze it. So for this project I used python to scrape the data and analyze it. All the code is contained in notebooks. I learned Python from Data Science courses using Jupyter Notebooks, so that's what I'm most comfortable with.

## Files

### get_data.ipynb
The data scraped comes from the diary page. The list of foods and notes was scraped into food_diary.csv. The daily nutrients was scraped into daily_data.csv. And for each food item in the diary Selenium was used to right click the food item, click on the detail link. Then the nutrient information from the details page was scraped into food_details.csv.

### data cleaning.ipynb
Data was cleaned. The data in food_diary.csv and food_details.csv was merged and stored in daily_foods_clean.csv. The cleaned data from daily_data.csv was stored as daily_clean.csv.

### Data Cleaning Part 2.ipynb
In this short notebook I looked for outliers. I ended up removing data for 06/06/21 and 06/09/21 because they were incomplete.

### EDA 2.ipynb
Finally the fun part! I was able to derive useful, to me at least, information out of the data. This is without any fancy math or machine learning. Just pandas and seaborn.
