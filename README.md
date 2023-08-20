# Netflix_Data_Analysis

 The provided code is a Python script that performs data analysis and visualization on a dataset of Netflix titles. The script uses the Pandas library for data manipulation and the Plotly library for creating interactive visualizations. Let's break down the code step by step:

Data Loading:

The code begins by importing necessary libraries, including Pandas for data manipulation and Plotly for visualization.
The dataset is loaded using Pandas' read_csv function from a CSV file named "netflix_titles_nov_2019.csv".
The first few rows of the dataset are displayed using the head() function to get a glimpse of the data.
Data Manipulation:

The 'date_added' column is converted to datetime format using pd.to_datetime. This ensures that the dates are treated as proper datetime objects for easier manipulation.
New columns 'year_added' and 'month_added' are created using the .dt.year and .dt.month methods, respectively, to extract the year and month components from the 'date_added' column.
Two new columns, 'season_count' and 'duration', are created using the apply function and lambda functions. 'season_count' stores the number of seasons for TV shows, and 'duration' stores the duration of movies. The values are extracted from the 'duration' column.
Content Type Analysis:

The code creates a pie chart using Plotly's go.Pie to show the distribution of content types (TV shows and movies) based on the 'type' column.
Content Added Over the Years:

Two DataFrames, 'd1' (for TV shows) and 'd2' (for movies), are created by filtering the main DataFrame based on the 'type' column.
The code generates line plots using Plotly's Scatter to visualize how content has been added over the years for both TV shows and movies.
Distribution of Release Years:

Similar to the previous step, the code creates bar plots using Plotly's Bar to display the distribution of content based on their release years for both TV shows and movies.
Month-wise Content Addition:

Bar plots are used to show which months have the highest number of content additions. The distribution of TV shows' additions in each month is shown using a single bar chart.
Geographical Content Analysis:

The geoplot function is defined to create a choropleth map using Plotly. This map represents the distribution of content across different countries. The 'country' column is processed to count content from each country.
The most common countries are displayed in a bar chart titled "Countries with most content."
Distribution of Movie Durations:

A distribution plot is created using Plotly's create_distplot to visualize the distribution of movie durations. The plot displays the density of durations using a KDE curve.
Categories of Content:

The code creates a bar chart to show the distribution of content across different categories. Categories are extracted from the 'listed_in' column.
Distribution of Content Ratings:

Bar charts are used to visualize the distribution of content ratings for both TV shows and movies.
Top Indian Movie Directors:
A specific analysis is performed on Indian movies. The code filters the data to include only Indian movies and creates a bar chart to display the directors from India with the most movie content.
Overall, this code performs a comprehensive analysis of the Netflix dataset, extracting insights on content types, release years, countries, genres, ratings, and more. It uses interactive Plotly visualizations to help convey these insights effectively. The code showcases the use of Pandas for data manipulation and Plotly for creating interactive and informative visualizations.
