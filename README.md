# Mars Web Scraping and Data Analysis  

## Background  

This project focuses on web scraping and data analysis skills by extracting and analyzing information from two web sources related to Mars. The project is divided into two parts:  

1. **Scraping Titles and Preview Text from Mars News Articles**  
2. **Scraping and Analyzing Mars Weather Data**  

These deliverables involve collecting data using **Beautiful Soup** and **Splinter**, organizing it into structured formats like Pandas DataFrames, and performing meaningful analyses to extract insights.  

---

## Repository Structure  

The repository contains the following files and folders:  

```  
mars-web-scraping/  
│  
├── Resources/                  # Folder containing any data files or scraped outputs  
│   ├── mars_weather.csv        # Scraped Mars weather data (output from Part 2)  
│   └── mars_news.json          # Scraped Mars news articles (optional output from Part 1)  
│  
├── part_1_mars_news.ipynb      # Jupyter Notebook for scraping Mars news articles  
├── part_2_mars_weather.ipynb   # Jupyter Notebook for scraping and analyzing Mars weather data  
├── README.md                   # Project README file  
├── requirements.txt            # Python dependencies  
├── .gitignore                  # File to exclude unnecessary files from version control  
│  
└── screenshots/                # Folder containing screenshots of results or plots (optional)  
    ├── mars_news_sample.png    # Sample screenshot of Mars news output  
    ├── mars_weather_plot.png   # Sample screenshot of weather analysis plot  
```  

---

## Objectives  

### Part 1: Scraping Mars News Articles  

In the first part, we scrape news articles from the [Mars News Website](https://redplanetscience.com) using automated browsing with Splinter and HTML parsing with Beautiful Soup. The goal is to extract:  

- **Titles** of the news articles.  
- **Preview text** corresponding to each title.  

The data is stored in a list of dictionaries, with each dictionary containing the following structure:  
```python  
{  
    'title': "Sample Title",  
    'preview': "Sample preview text."  
}  
```  

### Part 2: Scraping and Analyzing Mars Weather Data  

In the second part, we scrape a table of Mars weather data from the [Mars Temperature Data Site](https://static.bc-edx.com/data/web/mars_facts/temperature.html) and analyze it to answer key questions about Martian weather and climate.  

- The scraped data is stored in a Pandas DataFrame with the following columns:  
  - `id`: Unique identifier for the observation.  
  - `terrestrial_date`: Date on Earth corresponding to the observation.  
  - `sol`: The number of Martian days since the rover landed.  
  - `ls`: Solar longitude.  
  - `month`: Martian month.  
  - `min_temp`: Minimum temperature on Mars (°C).  
  - `pressure`: Atmospheric pressure at Curiosity's location.  

---  

## Instructions  

### Prerequisites  

1. Install Python 3.x.  
2. Install the required packages using the `requirements.txt` file:  
   ```bash  
   pip install -r requirements.txt  
   ```  

### Part 1: Scraping Mars News Articles  

1. Open the Jupyter Notebook `part_1_mars_news.ipynb`.  
2. Use Splinter to automate browsing and visit the Mars News site.  
3. Identify the HTML elements containing the news titles and previews using browser inspection tools.  
4. Use Beautiful Soup to scrape the titles and preview text.  
5. Store the data in a list of dictionaries and optionally export it to a JSON file.  

#### Sample Output  
```json  
[  
    {  
        "title": "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",  
        "preview": "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."  
    },  
    {  
        "title": "NASA's Perseverance Rover Collects Puzzle Pieces of Mars' History",  
        "preview": "The rover has been able to explore an area of the Red Planet that has a rich variety of rock textures and types."  
    }  
]  
```  

### Part 2: Scraping and Analyzing Mars Weather Data  

1. Open the Jupyter Notebook `part_2_mars_weather.ipynb`.  
2. Use Splinter and Beautiful Soup to scrape the Mars weather table.  
3. Convert the scraped data into a Pandas DataFrame.  
4. Perform the following analyses:  
   - Number of Martian months and days.  
   - Coldest and warmest months on Mars.  
   - Months with the lowest and highest atmospheric pressure.  
   - Approximate number of terrestrial days in a Martian year.  
5. Export the DataFrame to a CSV file for sharing or further analysis.  

#### Analysis Results  

1. **Coldest and Warmest Months**  
   Plot a bar chart showing average minimum temperatures by month.  

2. **Pressure Analysis**  
   Plot a bar chart showing average atmospheric pressure by month.  

3. **Martian Year Estimate**  
   Plot daily minimum temperatures to estimate the length of a Martian year.  

---

## Example Plots  

### 1. Average Minimum Temperature by Month  
![Coldest and Warmest Months](screenshots/mars_temp_plot.png)  

### 2. Average Atmospheric Pressure by Month  
![Pressure Analysis](screenshots/mars_pressure_plot.png)  

---

## Key Findings  

- **Coldest Month**: Month X had the lowest average minimum temperature of -XX°C.  
- **Warmest Month**: Month Y had the highest average minimum temperature of XX°C.  
- **Lowest Pressure**: Month Z had the lowest average pressure of XX hPa.  
- **Highest Pressure**: Month W had the highest average pressure of XX hPa.  
- **Martian Year**: Approximately X terrestrial days.  
