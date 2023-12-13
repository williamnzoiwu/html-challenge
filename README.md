# html-challenge
## HTML Module 11 Challenge
This code contains two Jupyter notebooks scraping data from a news site.

### Part 1: Mars News
This script first uses automated browsing to visit the Mars news website in a new Chrome window. It then creates a Beautiful Soup object named "soup" to extract text elements from the website. It then creates an empty list to store the title and preview element from the scraped text data. Both elements are stored as a title-and-preview pair in a Python dictionary, each with two keys: title and preview. The dictionaries are then stored in the empty list, and the list is then printed.

### Part 2: Mars Weather
The second notebook also first uses automated browsing to visit a the Mars Temperature Data SiteLinks website in a new Chrome window. It then creates a Beautiful Soup object and uses it to scrape the data in the HTML table. The scraped data is the put into a Pandas DataFrame with the same column headings as the table on the website. The column descriptions are as follows:

id: the identification number of a single transmission from the Curiosity rover
terrestrial_date: the date on Earth

sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars

ls: the solar longitude

month: the Martian month

min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)

pressure: The atmospheric pressure at Curiosity's location

All the data types are defaulted as objects, so the script then changes the majority of the data types: the "terrestrial_date" column is changed to datetime, the "ls", "sol", and "month" columns are changed to integers, and the "min_temp" and "pressure" columns are changed to floats. The dataset is then analyzed by using Pandas functions to answer the following questions:

How many months exist on Mars? (This is answered by using a groupby and a count of the "month" column.)

How many Martian days worth of data exist in the scraped dataset? (This is done by simply counting the rows of data.)

What are the coldest and the warmest months on Mars? (This is answered by getting the average min temperature for each month, and then seeing which month the lowest temperature and which month has the highest.)

Which months have the lowest and the highest atmospheric pressure on Mars? (This is answered very similarly to the last one, just taking the average pressure for each month instead of the temperature.)

About how many terrestrial (Earth) days exist in a Martian year? (This is displayed by plotting the daily minimum temperature across the whole dataset.)

Lastly, after all of the analysis is done, the DataFrame is exported to a CSV file.
