# html-challenge
## HTML Module 11 Challenge
This code contains two Jupyter notebooks scraping data from a news site.

### Part 1: Mars News
This script first uses automated browsing to visit the Mars news website. It then creates a Beautiful Soup object named "soup" to extract text elements from the website. It then creates an empty list to store the title and preview element from the scraped text data. Both elements are stored as a title-and-preview pair in a Python dictionary, each with two keys: title and preview. The dictionaries are then stored in the empty list, and the list is then printed.

### Part 2: Mars Weather
The second notebook also first uses automated browsing to visit a the Mars Temperature Data SiteLinks website. It then creates a Beautiful Soup object and uses it to scrape the data in the HTML table. The scraped data is the put into a Pandas DataFrame with the same column headings as the table on the website. The column descriptions are as follows:

id: the identification number of a single transmission from the Curiosity rover
terrestrial_date: the date on Earth

sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars

ls: the solar longitude

month: the Martian month

min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)

pressure: The atmospheric pressure at Curiosity's location

All the data types are defaulted as objects, so the script then changes the majority of the data types: the "terrestrial_date" column is changed to datetime, the "ls", "sol", and "month" columns are changed to integers, and the "min_temp" and "pressure" columns are changed to floats. The dataset is then analyzed by using Pandas functions to answer the following questions:

How many months exist on Mars? (This is asnwered by using a groupby and then a count of the "month" column.)

How many Martian (and not Earth) days worth of data exist in the scraped dataset?

What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:

Find the average minimum daily temperature for all of the months.
Plot the results as a bar chart.

Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
Find the average daily atmospheric pressure of all the months.
Plot the results as a bar chart.

About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
Consider how many days elapse on Earth in the time that Mars circles the Sun once.
Visually estimate the result by plotting the daily minimum temperature.

Lastly, the DataFrame is exported to a CSV file.
