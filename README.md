# Climate Analysis Dashboard:

## Background:

* The website created for this project was drawn directly from the work done in the WeatherPy project. Where I created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I utilized Python libraries such as Pandas, Matplotlib, Numpy, Requests, and Datetime, the OpenWeatherMap API, and a little common sense to create a representative model of weather across world cities. This responsive website contains 7 total pages that provide insight into the analysis, visualizations and dataset.

* The following scatter plots were then created via Matplotlib to showcase the following relationships:

  * Temperature (F) vs. Latitude
  * Humidity (%) vs. Latitude
  * Cloudiness (%) vs. Latitude
  * Wind Speed (mph) vs. Latitude
  
* While planning and developing the HTML/CSS for this Dashboard, I soon realized that I would like to utilize Python's Datetime functions to transform the "Date" for the dataset from an INT64 to a Datetime object. However, while transforming and reviewing the "Date" column I noticed that the values held within the CSV file provided to us by the Program did not match the "Date" listed in each of the four visualizations. I, therefore, chose to extract the dataset used in the WeatherPy project, transform the column name for "City_ID" and reformat the "Date" column as a Datetime object via Pandas. I also chose to strip the time portion of the Datetime object for readability. Once this was completed, I recreated the scatter plots, originally used in the previous project, in-order to edit some of the colors so that they match the Website/Dashboard style.

## Directory:

* Landing Page ---> index.html:

   * An explanation of the project.
  
   * Links to each visualization.
  
* Visualization Pages:

   * Max Temperature vs. Latitude ---> max_temperature.html
   * Humidity vs. Latitude ---> humidity.html
   * Cloudiness vs. Latitude ---> cloudiness.html
   * Wind Speed vs. Latitude ---> wind_speed.html

     * A descriptive title and heading tag.
  
     * The plot/visualization itself for the selected comparison.
  
     * A paragraph describing the plot and its significance.
     
* Comparisons Page ---> comparisons.html

   * Contains all visualizations on the same page for easier visual comparison.
   
   * Uses bootstrap grid for the visualizations.
     
* Data Page ---> data.html

   * Displays a resonsive table containing the data used in the visualizations.
   
     * Bootstrap table component.
     
* Style ---> style.css

   * Contains both custom styles and styles generated via Bootstrap.
   
   * Includes CSS media query for the navigation menu.
   
* Jupyter Notbook ---> lat_data_conversion.ipynb

   * Utilizes Pandas, Numpy, Datetime and Matplotlib.pyplot.
   
   * Extracts CSV via Pandas' read_csv.
   
   * Checks Data Types.
   
   * Transformation:
   
      * Converts "Date" column to Datetime.
      
      * Strips time to Date only.
      
      * Renames City_ID column.
      
   * Converts Dataframe to HTML and loads to data_all.html.
   
      * HTML code cut and pasted into data.html ---> data_all.html deleted
      
   * Creates 4 total visualizations (scatter plots), overwrites existing images, and referenced in HTML code.

* Resources (Folder):

  * Data ---> weather_data.csv
  
     * Datset contains the weather of 500+ cities across the world of varying distance from the equator, pulled from the OpenWeatherMap API on 07/06/2019.
     
  * assets (Folder):
  
    * images (Folder):
    
      1. City Latitude vs. Max Temperature 07/06/2019 ---> Fig1.png
      2. City Latitude vs. Humidity 07/06/2019 ---> Fig2.png
      3. City Latitude vs. Cloudiness 07/06/2019 ---> Fig3.png
      4. City Latitude vs. Wind Speed 07/06/2019 ---> Fig4.png
