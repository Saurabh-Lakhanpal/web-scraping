# web-scraping

Identify HTML elements on a page, identify their id and class attributes, and use this to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. Use web-scraping to extract HTML tables or recurring elements, like multiple news articles on a webpage, and analyze the data.

Steps done are collecting data, organizing and storing data, analyzing data, and then visually communicating insights.
- Scrape titles and preview text from Mars news articles.
- Scrape and analyze Mars weather data, which exists in a table.

## Solution
- [mars_news](https://github.com/Saurabh-Lakhanpal/web-scraping/blob/main/mars_news.ipynb)
- [mars_weather](https://github.com/Saurabh-Lakhanpal/web-scraping/blob/main/mars_weather.ipynb)
- Source - [News - Mars Exploration Program](https://static.bc-edx.com/data/web/mars_news/index.html)

## Instructions

### Part 1: Scrape Titles and Preview Text from Mars News

1. Use Jupyter Notebook to scrape the [Mars News](https://static.bc-edx.com/data/web/mars_news/index.html) webpages.
2. Use automated browsing to visit the Mars news siteLinks to an external site. Inspect the page to identify which elements to scrape. By Creating a Beautiful Soup object and use it to extract text elements from the website.
3. Extract the titles and preview text of the news articles that are scraped. Store the scraping results in Python data structures as follows:
   - Each title-and-preview pair in a Python dictionary and, give each dictionary two keys: `title` and `preview`. An example is the following:
     ```python
     {
       'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",
       'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."
     }
     ```
   - Store all the dictionaries in a Python list.
   - Print the list in the notebook.
   - Optionally, store the scraped data in a file by exporting the scraped data to a JSON file.

### Part 2: Scrape and Analyze Mars Weather Data

1. Use Jupyter Notebook to scrape and analyze [Mars weather](https://static.bc-edx.com/data/web/mars_facts/temperature.html) data.
2. Use automated browsing to visit the Mars Temperature Data SiteLinks to an external site. Inspect the page to identify which elements to scrape from the webpage. Create a Beautiful Soup object and use it to scrape the data in the HTML table.
3. Assemble the scraped data into a Pandas DataFrame. The columns to have the same headings as the table on the website. Explanation of the column headings:
   - `id`: the identification number of a single transmission from the Curiosity rover
   - `terrestrial_date`: the date on Earth
   - `sol`: the number of elapsed sols (Martian days) since Curiosity landed on Mars
   - `ls`: the solar longitude
   - `month`: the Martian month
   - `min_temp`: the minimum temperature, in Celsius, of a single Martian day (sol)
   - `pressure`: The atmospheric pressure at Curiosity's location
4. Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate `datetime`, `int`, or `float` data types.
Analyze the dataset by using Pandas functions to answer the following questions:
    - How many months exist on Mars?
    - How many Martian (and not Earth) days worth of data exist in the scraped dataset?
    - What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
    - Find the average minimum daily temperature for all of the months.
    - Plot the results as a bar chart.
    - Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
    - Find the average daily atmospheric pressure of all the months.
    - Plot the results as a bar chart.
    - About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
    - Consider how many days elapse on Earth in the time that Mars circles the Sun once.
    - Visually estimate the result by plotting the daily minimum temperature of each observation.
    - Export the DataFrame to a CSV file.
