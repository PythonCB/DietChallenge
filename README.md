# DietChallenge
In this project I scrape data from cronometer.com and analyze it. From April 1st 2021 to August 14th 2021 I tracked everything I ate, my daily weight, and my exercise on cronometer. I always wondered what I could learn if I could scrape that data and analyze it. All the code is in Python. I used Selenium to log into and navigate cronometer and Pandas for the scraping and data analysis. I wrote an article about the code and what I learned from analyzing the data which can be found [here](https://blog.finxter.com/how-i-scraped-my-nutrition-data-from-cronometer-com/)

My goal for the project was to demonstrate that there is value to be had in scraping and analyzing data relating to a personal goal. I'd say it was a success. I lost over 20 pounds slowly and safely. What I found most interesting about the data is just how linear the weight loss was over the long run. From day to day the weight loss seemed to be almost random. I could do everything right on some days and gain a pound the next morning. But it averaged out in the long run.

![image](https://github.com/PythonCB/DietChallenge/assets/106499531/da1c48d8-b7ed-4b4e-b90b-435613a07f2c)

That's pretty linear! 

## Cronometer
[cronometer](https://cronometer.com/) is a great site for tracking calories, exercise, macro and micro nutrients, weight etc. My goal was to hit 100% of the US recommended daily allowance of all the vitamins and minerals in addition to trying to hit a daily caloric deficit of at least 100 calories. The estimates of calories burned each day is not very precise so I tried to err on the side of underestimating the calories I burned and overestimating what I ate each day. As a result, the caloric deficit functions as more of a signal than a precise measurement. But the process worked, so I am happy :)

![image](https://github.com/PythonCB/DietChallenge/assets/106499531/7c46a437-c3fc-43ac-8c02-e6359d2b3234)


## Files

### get_data.ipynb
The data scraped comes from the diary page. The list of foods and notes was scraped into food_diary.csv. The daily nutrients was scraped into daily_data.csv. And for each food item in the diary Selenium was used to right click the food item, click on the detail link. Then the nutrient information from the details page was scraped into food_details.csv.

### data cleaning.ipynb
Data was cleaned. The data in food_diary.csv and food_details.csv was merged and stored in daily_foods_clean.csv. The cleaned data from daily_data.csv was stored as daily_clean.csv.

### Data Cleaning Part 2.ipynb
In this short notebook I looked for outliers. I ended up removing data for 06/06/21 and 06/09/21 because they were incomplete.

### EDA 2.ipynb
Finally the fun part! I was able to derive useful, to me at least, information out of the data. This is without any fancy math or machine learning. Just pandas and seaborn.
