# Mars News and Weather Data Web-Scraping Project

## Overview
This project demonstrates the process of web scraping and data analysis by extracting and analyzing data related to Mars. The assignment consists of two main deliverables:

1. **Scraping Titles and Preview Text from Mars News Articles**: Extracting the latest Mars news articles, including their titles and preview text, and storing them in a structured format.
2. **Scraping and Analyzing Mars Weather Data**: Extracting Mars weather data from an HTML table, organizing it in a Pandas DataFrame, analyzing trends, and visualizing insights.

---

## Deliverables

### Deliverable 1: Scrape Titles and Preview Text from Mars News
- **Automated Browsing**: Uses Splinter to navigate the Mars News website.
- **Data Extraction**: Extracts titles and preview text for multiple Mars news articles using Beautiful Soup.
- **Data Storage**:
  - The scraped data is stored as a list of dictionaries, where each dictionary contains:
    - `title`: Title of the article.
    - `preview`: Preview text of the article.
  - Example:
    ```python
    {
        'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",
        'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."
    }
    ```
- **Output**:
  - Prints the list of dictionaries in the notebook.
  - Optionally exports the data to a JSON file for sharing.

---

### Deliverable 2: Scrape and Analyze Mars Weather Data
- **Web Scraping**:
  - Scrapes Mars weather data using Beautiful Soup to extract data from an HTML table.
  - Data includes columns:
    - `id`: Transmission identification number.
    - `terrestrial_date`: Date on Earth.
    - `sol`: Elapsed sols (Martian days).
    - `ls`: Solar longitude.
    - `month`: Martian month.
    - `min_temp`: Minimum daily temperature (°C).
    - `pressure`: Atmospheric pressure.
  - Assembles the data into a Pandas DataFrame with proper column names.

- **Data Processing**:
  - Converts column data types for accurate analysis:
    - `terrestrial_date`: Datetime format.
    - Numerical columns: Integer or float format.
  - Exports the DataFrame to a CSV file.

- **Analysis**:
  - Answers key questions:
    1. **How many months exist on Mars?**
    2. **How many Martian days' worth of data exist?**
    3. **Which month has the lowest/highest average temperature?** (Visualized as a bar chart.)
    4. **Which month has the lowest/highest atmospheric pressure?** (Visualized as a bar chart.)
    5. **How many Earth days exist in a Martian year?** (Estimated visually by plotting minimum daily temperature.)

---

## Visualizations
The project includes the following visualizations:
1. **Daily Minimum Temperature**:
   - Displays the minimum temperature trends over Martian days.
   - Highlights temperature restart points with vertical dashed lines for clarity.

2. **Average Monthly Temperature**:
   - Bar chart showing average minimum temperatures across months.
   - Identifies coldest and warmest months.

3. **Average Monthly Pressure**:
   - Bar chart showing average atmospheric pressure across months.
   - Highlights months with the lowest and highest pressure.

---

## File Structure
- **part_1_mars_news.ipynb**: Jupyter Notebook for scraping Mars News articles.
- **part_2_mars_weather.ipynb**: Jupyter Notebook for scraping and analyzing Mars Weather data.
- **scraped_data.json** (Optional): JSON file with extracted Mars News data.
- **mars_weather_data.csv**: CSV file containing processed Mars Weather data.

---

## Key Insights
- There are 12 months on Mars, with varying temperature and pressure conditions.
- The Martian year consists of approximately 687 Earth days, as derived from temperature cycle patterns.
- Visualizations reveal patterns and provide insights into Martian weather cycles.

---

## How to Run
1. Clone the repository containing the project files.
2. Open the Jupyter Notebooks (`part_1_mars_news.ipynb` and `part_2_mars_weather.ipynb`) in Visual Studio Code or another environment.
3. Run the code cells step by step to reproduce the scraping and analysis processes.
4. Explore the visualizations and CSV outputs for insights.

---

## Tools Used
- **Splinter**: For automated browsing and navigating websites.
- **Beautiful Soup**: For HTML parsing and data extraction.
- **Pandas**: For organizing, processing, and analyzing data.
- **Matplotlib**: For creating insightful visualizations.

---

## Final Notes
This project showcases the power of web scraping and data analysis to extract valuable information from online sources and visualize trends. It strengthens essential skills in data collection, storage, processing, and communication.

Happy grading!
