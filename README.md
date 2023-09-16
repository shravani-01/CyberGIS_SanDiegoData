# CyberGIS_SanDiegoData

 Map Dictionary
1. Visualizing the Impact of Covid-19: Temporal Trends in Crude and Vaccination Rates by Zip Code in San Diego (ACM_COVID_MLC_SD)
Link:
https://drive.google.com/file/d/1EK3WSMiQ6k5U9DjrUZrPgYaHu2eTmEnX/view?usp=drive_link
Dashboard Summary:
Title: Visualizing the Impact of Covid-19 in San Diego:
This interactive dashboard utilizes the Adaptive Choropleth Mapper (ACM) library to visualize and analyze the impact of Covid-19 in San Diego. The data for visualization is sourced from the "SD_Confirmed_Vaccine_Final_v5.csv" dataset, containing crucial variables such as geo IDs, confirmed cases, vaccination rates, and other Covid-19 metrics. Additionally, geographical coordinates of San Diego places are loaded from the "SanDiego_Zip_COVID.shp" shapefile using the geospatial library, Geopandas.
The dashboard's primary objective is to provide an insightful analysis of Covid-19 trends and vaccination rates across different zip codes in San Diego. It offers a user-friendly interface with multiple linked charts to facilitate data exploration and comparison. The dashboard comprises two side-by-side choropleth maps, a bar chart, and temporal line charts that enable users to gain a comprehensive understanding of the pandemic's impact on various regions.
Functions and Key Concepts:
Data Loading and Preparation:
● The pd.read_csv() function is used to load Covid-19 data from the CSV file, and the gpd.read_file() function is used to load the geometrical coordinates of San Diego places from the shapefile.
● Data types of specific columns are adjusted to ensure proper handling of the data.
  
 ● Columns are renamed for better understanding and consistency. ACM Visualization Parameters:
● The param_MLC_COVID dictionary contains several parameters that customize the ACM dashboard.
● Key parameters include the title and subject of the dashboard, the filename suffix, and the data sources (Covid DataFrame and shapefile_SD GeoDataFrame).
● The periods parameter is set to "All," allowing visualization of data from all available time periods.
● The variables list contains the variable names to be visualized on the map, such as "Confirmed_Cases_per_10k_pop" and "vaccinated_per_10k_pop".
● The NumOfMaps parameter sets the number of side-by-side maps for comparison, which is two in this case.
● The InitialLayers parameter sets the initial layers (variables) to be displayed on the map when the dashboard loads.
● The Initial_map_center and Initial_map_zoom_level parameters set the initial geographical center and zoom level of the map.
● The Map_width and Map_height parameters determine the dimensions of the map in the dashboard.
● The Top10_Chart parameter is set to True, enabling the display of a bar chart showing the top 10 places with the highest values for the selected variable.
● The Multiple_Line_Chart parameter is also set to True, allowing the display of multiple temporal line charts for trend analysis.
● The NumOfMLC parameter specifies the number of multiple line charts to be displayed.
● The titlesOfMLC list provides titles for each of the multiple line charts to give context to the visualization.
● The DefaultRegion_MLC parameter sets the default region (zip code) to be displayed in the multiple line charts.
Creating the Dashboard:
● The Adaptive_Choropleth_Mapper_viz function is used to generate the
interactive dashboard based on the parameters defined in param_MLC_COVID.
● The Adaptive_Choropleth_Mapper_log function is used to log user interactions
and activities on the dashboard, capturing important insights and feedback.
The first component of the dashboard consists of two choropleth maps. Users can compare different layers of data by selecting specific variables from the available options, such as confirmed cases per 10,000 population and vaccination rates. This visual representation allows for an intuitive examination of how Covid-19 metrics have evolved over time across different zip codes in San Diego.

 To provide deeper insights, the dashboard incorporates a bar chart showcasing the top 10 regions with the highest values for the selected variable. This feature aids in identifying hotspots and areas that may require special attention in terms of Covid-19 control measures or vaccination efforts.
Furthermore, the dashboard offers a set of temporal line charts. These dynamic charts permit users to analyze and compare trends in Covid-19 cases, vaccination rates, and other metrics over time for multiple zip codes simultaneously. This comprehensive time-series analysis enables the identification of temporal patterns and helps discern potential correlations between Covid-19 metrics and vaccination rates.
Users can easily interact with the dashboard, selecting different variables, zip codes, and periods to focus on specific aspects of the data. By harnessing the power of data visualization and interactive exploration, this dashboard serves as a valuable tool for policymakers, researchers, and the public to gain valuable insights into the evolving Covid-19 situation in San Diego and make informed decisions to combat the pandemic effectively.
2.Visualizing the Impact of Covid-19: Comparing Crude Rates across San Diego Zip Codes Over Time
Link:
https://drive.google.com/file/d/1FLXNJ9ZWvZz7n3fPdevXtB498urajhem/view?usp=drive_link
Dashboard Summary: Visualizing Covid-19 Crude Rates Across San Diego Zip Codes Over Time
This interactive dashboard utilizes the Adaptive Choropleth Mapper (ACM) library to visualize and compare the impact of Covid-19 crude rates across different zip codes in San Diego over time. The data for visualization is sourced from the "SD_Confirmed_Vaccine_Final_v5.csv" dataset, which contains relevant variables such as geo IDs and confirmed cases per 10,000 population. The geographical coordinates of San Diego places are loaded from the "SanDiego_Zip_COVID.shp" shapefile using the geospatial library, Geopandas.
Functions and Key Concepts:
Dashboard Objective:
 
 ● The primary goal of this dashboard is to provide a temporal comparison of Covid-19 crude rates across San Diego zip codes. By visualizing the data over time, the dashboard enables users to identify trends and patterns in Covid-19 cases within specific regions.
Data Loading and Preparation:
● The pd.read_csv() function is used to load Covid-19 data from the CSV file, and
the gpd.read_file() function is used to load the geometrical coordinates of San
Diego places from the shapefile.
● Data types of specific columns are adjusted to ensure proper handling of the
data.
● Columns are renamed for better understanding and consistency.
ACM Visualization Parameters:
● The param_CLC_COVID1 dictionary contains various parameters to customize
the ACM dashboard.
● Key parameters include the title and subject of the dashboard, the filename
suffix, and the data sources (Covid DataFrame and shapefile_SD
GeoDataFrame).
● The periods parameter is set to "All," allowing visualization of data from all
available time periods.
● The variables list contains the variable name "Confirmed_Cases_per_10k_pop,"
representing the Covid-19 confirmed cases per 10,000 population.
● The NumOfMaps parameter sets the number of side-by-side maps for
comparison, which is two in this case.
● The InitialLayers parameter sets the initial layers (dates) to be displayed on the
map when the dashboard loads.
● The Initial_map_center and Initial_map_zoom_level parameters set the initial
geographical center and zoom level of the map.
● The Map_width and Map_height parameters determine the dimensions of the
map in the dashboard.
● The Top10_Chart parameter is set to True, enabling the display of a bar chart
showing the top 10 zip codes with the highest confirmed cases per 10,000
population.
● The Comparision_Chart parameter is set to True, allowing the display of a chart
for temporal comparisons of crude rates across selected zip codes.
● The DefaultRegion_CLC parameter specifies the default zip codes to be displayed in the comparison chart, providing users with a starting point for their
analysis.
Creating the Dashboard:
● The Adaptive_Choropleth_Mapper_viz function is used to generate the
interactive dashboard based on the parameters defined in param_CLC_COVID1.

 ● The Adaptive_Choropleth_Mapper_log function is used to log user interactions and activities on the dashboard, capturing important insights and feedback.
In summary, this interactive dashboard provides an in-depth comparison of Covid-19 crude rates across San Diego zip codes over time. Users can interactively explore the data on choropleth maps and examine trends using the comparison chart. The dashboard empowers users to make data-driven decisions and gain valuable insights into the progression of Covid-19 cases in different regions of San Diego, contributing to a more informed and effective response to the pandemic.
3. Visualizing Covid-19 Vaccination Trends Across Zip Codes in San Diego Over Time
Link: https://drive.google.com/file/d/1_wT78jS54IsvFjtu3045xIeXaKmfvBJy/view?usp=drive_link Dashboard Summary: Visualizing Covid-19 Vaccination Trends Across San Diego Zip Codes Over
Time
This interactive dashboard leverages the Adaptive Choropleth Mapper (ACM) library to visualize and compare Covid-19 vaccination trends across different zip codes in San Diego over time. The data for visualization is sourced from the "Vaccine" dataset, which contains relevant variables such as vaccination rates per 10,000 population. Geographical coordinates of San Diego places are loaded from the "SanDiego_Zip_COVID.shp" shapefile using the geospatial library, Geopandas.
Functions and Key Concepts:
Dashboard Objective:
● The primary objective of this dashboard is to provide a visual comparison of
Covid-19 vaccination rates across different zip codes in San Diego over time. Users can interactively explore vaccination trends and identify variations in vaccine coverage among various regions.
Data Loading and Preparation:
● The pd.read_csv() function is used to load vaccination data from the CSV file, and the gpd.read_file() function is used to load the geometrical coordinates of San Diego places from the shapefile.
● Data types of specific columns are adjusted to ensure proper handling of the data.
● Columns are renamed for better understanding and consistency.
 
 ACM Visualization Parameters:
● The param_CLC_COVID2 dictionary contains various parameters to customize
the ACM dashboard.
● Key parameters include the title and subject of the dashboard, the filename
suffix, and the data sources (Vaccine DataFrame and shapefile_SD
GeoDataFrame).
● The periods parameter is set to "All," allowing visualization of data from all
available time periods.
● The variables list contains the variable name "vaccinated_per_10k_pop,"
representing the Covid-19 vaccination rates per 10,000 population.
● The NumOfMaps parameter sets the number of side-by-side maps for
comparison, which is two in this case.
● The InitialLayers parameter sets the initial layers (dates) to be displayed on the
map when the dashboard loads.
● The Initial_map_center and Initial_map_zoom_level parameters set the initial
geographical center and zoom level of the map.
● The Map_width and Map_height parameters determine the dimensions of the
map in the dashboard.
● The Top10_Chart parameter is set to True, enabling the display of a bar chart
showing the top 10 zip codes with the highest vaccination rates per 10,000
population.
● The Comparision_Chart parameter is set to True, allowing the display of a chart
for temporal comparisons of vaccination rates across selected zip codes.
● The DefaultRegion_CLC parameter specifies the default zip codes to be displayed in the comparison chart, providing users with a starting point for their
analysis. Creating the Dashboard:
● The Adaptive_Choropleth_Mapper_viz function is used to generate the interactive dashboard based on the parameters defined in param_CLC_COVID2.
● The Adaptive_Choropleth_Mapper_log function is used to log user interactions
and activities on the dashboard, capturing important insights and feedback.
In conclusion, this interactive dashboard offers a comprehensive view of Covid-19 vaccination trends across San Diego zip codes over time. Users can visually compare vaccination rates using choropleth maps and analyze temporal changes through the comparison chart. The dashboard empowers users to make data-driven decisions, identify areas with higher vaccination rates, and track the progress of vaccination efforts in different regions of San Diego.
4. Temporal Patterns of Covid-19 Crude Rate and Vaccinated Rate at Zip Code Level in US Counties
Link: https://drive.google.com/file/d/1_e2ajrY4bYcqBZMLw2KiCmzxDLPVzDZQ/view?usp=drive_link
 
 Dashboard Summary: Temporal Patterns of Covid-19 Crude Rate and Vaccinated Rate in US Counties
This interactive dashboard utilizes the Adaptive Choropleth Mapper (ACM) library to visualize and analyze temporal patterns of Covid-19 crude rate and vaccinated rate at the zip code level in US counties for the year 2020. The data for visualization is sourced from the "Covid_Rate_daily_counties_mainland.csv" dataset, which includes essential variables such as geo IDs, confirmed rate, death rate, and cumulative rates. Additionally, the geographical coordinates of US counties are loaded from the "counties.shp" shapefile using the geospatial library, Geopandas.
Functions and Key Concepts: Dashboard Objective:
● The main objective of this dashboard is to provide a comprehensive understanding of temporal patterns in Covid-19 crude rate and vaccinated rate across US counties at the zip code level throughout the year 2020. By visualizing and analyzing these temporal patterns, users can identify trends and variations in Covid-19 metrics.
Data Loading and Preparation:
● The pd.read_csv() function is used to load Covid-19 data from the CSV file, and
the gpd.read_file() function is used to load the geometrical coordinates of US
counties from the shapefile.
● Data types of specific columns are adjusted to ensure proper handling of the
data.
● Columns are renamed for better understanding and consistency.
ACM Visualization Parameters:
● The param_MLC_COVID_US_2020 dictionary contains various parameters to
customize the ACM dashboard.
● Key parameters include the title and subject of the dashboard, the filename
suffix, and the data sources (Covid_2020 DataFrame and shapefile_US
GeoDataFrame).
● The periods parameter is set to "All," allowing visualization of data from all
available time periods in the year 2020.
● The variables list contains the variable names "confirmed_rate," "death_rate,"
"confirmed_rate_total," and "death_rate_total," representing Covid-19 confirmed rate, death rate, cumulative confirmed rate, and cumulative death rate per 10,000 population, respectively.

 ● The NumOfMaps parameter sets the number of side-by-side maps for comparison, which is two in this case.
● The InitialLayers parameter sets the initial layers (dates) to be displayed on the map when the dashboard loads.
● The Initial_map_center and Initial_map_zoom_level parameters set the initial geographical center and zoom level of the map.
● The Map_width and Map_height parameters determine the dimensions of the map in the dashboard.
● The Top10_Chart parameter is set to True, enabling the display of a bar chart showing the top 10 counties with the highest Covid-19 confirmed rates per 10,000 population.
● The Multiple_Line_Chart parameter is also set to True, allowing the display of multiple temporal line charts for trend analysis.
● The NumOfMLC parameter specifies the number of multiple line charts to be displayed.
● The titlesOfMLC list provides titles for each of the multiple line charts, offering context and insights for the visualization.
● The DefaultRegion_MLC parameter specifies the default county (zip code) to be displayed in the multiple line charts.
Creating the Dashboard:
● The Adaptive_Choropleth_Mapper_viz function is used to generate the
interactive dashboard based on the parameters defined in param_MLC_COVID_US_2020.
In conclusion, this interactive dashboard provides a detailed analysis of Covid-19 crude rate and vaccinated rate trends in US counties at the zip code level throughout 2020. Users can visually explore the data through choropleth maps and temporal line charts, identifying temporal patterns and trends in Covid-19 metrics. The dashboard empowers users to gain valuable insights into the pandemic's dynamics in various regions of the US, facilitating informed decision-making and response strategies.
5. Temporal Patterns of Covid-19 Crude Rate and Vaccinated Rate at Zip Code Level in US Counties
Link: https://drive.google.com/file/d/1VT4-uqxQztjQ0QlHoT04__C7AcWFX1Uv/view?usp=drive_link
 
 Dashboard Summary: Comparison of Temporal Patterns of Covid-19 Crude Rate Between US Counties
This interactive dashboard employs the Adaptive Choropleth Mapper (ACM) library to visualize and compare temporal patterns of Covid-19 crude rate among various US counties. The dataset used for visualization is "Covid_Rate_daily_counties_mainland.csv," which contains crucial variables such as geo IDs and Covid-19 confirmed rates. Geographical coordinates of US counties are loaded from the "counties.shp" shapefile using the geospatial library, Geopandas.
Functions and Key Concepts:
Dashboard Objective:
● The primary objective of this dashboard is to facilitate a comprehensive
comparison of temporal patterns in Covid-19 crude rate across different US counties. By visualizing these patterns over time, users can gain insights into the variations and trends in Covid-19 metrics among different regions.
Data Loading and Preparation:
● The pd.read_csv() function is used to load Covid-19 data from the CSV file, and
the gpd.read_file() function is used to load the geometrical coordinates of US
counties from the shapefile.
● Data types of specific columns are adjusted to ensure proper handling of the
data.
● Columns are renamed for better understanding and consistency.
ACM Visualization Parameters:
● The param_CLC_COVID3 dictionary contains various parameters to customize
the ACM dashboard.
● Key parameters include the title and subject of the dashboard, the filename
suffix, and the data sources (Covid_2020 DataFrame and shapefile_US
GeoDataFrame).
● The periods parameter is set to "All," allowing visualization of data from all
available time periods.
● The variables list contains the variable name "confirmed_rate," representing
Covid-19 confirmed rate per 10,000 population.
● The NumOfMaps parameter sets the number of side-by-side maps for
comparison, which is two in this case.
● The InitialLayers parameter sets the initial layers (dates) to be displayed on the
map when the dashboard loads.
● The Initial_map_center and Initial_map_zoom_level parameters set the initial
geographical center and zoom level of the map.

 ● The Map_width and Map_height parameters determine the dimensions of the map in the dashboard.
● The Top10_Chart parameter is set to True, enabling the display of a bar chart showing the top 10 counties with the highest Covid-19 confirmed rates per 10,000 population.
● The Comparision_Chart parameter is set to True, allowing the display of a chart for temporal comparisons of Covid-19 crude rates across selected counties.
● The DefaultRegion_CLC parameter specifies the default counties (geo IDs) to be displayed in the comparison chart, providing users with a starting point for their analysis.
Creating the Dashboard:
● The Adaptive_Choropleth_Mapper_viz function is used to generate the
interactive dashboard based on the parameters defined in param_CLC_COVID3.
In conclusion, this interactive dashboard offers a powerful tool for comparing temporal patterns of Covid-19 crude rates among various US counties. Users can explore the data through choropleth maps and temporal line charts, identifying trends and variations in Covid-19 metrics across different regions. The dashboard empowers users to make data-driven decisions and gain valuable insights into the dynamics of the pandemic in different parts of the United States, facilitating informed public health strategies and responses.
