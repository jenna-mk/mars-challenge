# Module 11 Challenge: Webscraping and Data Analysis 
The purpose of this challenge is to utilize Splinter and Beautiful Soup to scrape various types of information, such as HTML tables and recurring elements, from a webpage about Mars and perform an analysis on the scraped data.

## Part 1: Scrape Titles and Preview Text from Mars News 
The first part of this challenge involves scraping data from various Mars news articles. The first step is to create a Beautiful Soup object in order to scrape the title and preview from each article on the page. Each title and preview pair is stored as an individual Python dictionary, which is then stored in a Python list. The code for this part can be found in Starter_Code/part_1_mars_news_ipynb.

## Part 2: Scrape and Analyze Mars Weather Data
The second part of this challenge is to scrape the data collected by a Mars rover, which is stored in a table. First, I created a Beautiful Soup object to scrape the data, which includes the following columns:
* id (the identification number of a single transmission from the Curiosity rover)
* terrestrial_date (the date on Earth)
* sol (the number of elapsed Martian days since the Curiosity landed on Mars)
* ls (the solar longitude)
* month (the Martian month)
* min_temp (the minimum temperature in Celsius of a single Martian day)
* pressure (the atmospheric pressure at Curiosity's location)

After scraping the data, I examined the data type of each column and converted the data as follows:
* id converted to integer
* terrestrial_date converted to date_time
* sol converted to integer
* ls converted to integer
* month converted to integer
* min_temp converted to float
* pressure converted to float

Next, I used various Pandas functions to analyze the data and answer questions regarding temperature, pressure, and time. This analysis revealed that 
1.) There are 12 months on Mars.
2.) There are 1987 Martian days' worth of data in the table.
3.) The average low temperature by month ranges from -68 to -83 degrees Celsius (see plot in code).
4.) The hottest month on Mars is the 8th month; the coldest month on Mars is the 3rd month.
5.) The average pressure by month ranges from 745 to 913 atm (see plot in code).
6.) The 9th month is the month with the highest atmospheric pressure.
7.) One year on Mars (visual estimate) is approximately 680 days on Earth (see plots in code).

The data for this part is saved to Starter_Code/mars_data.csv and the full code for this part can be found in Starter_Code/part_2_mars_weather.ipynb.
