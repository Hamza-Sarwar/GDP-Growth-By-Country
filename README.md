# GDP-Growth-By-Country
Categorize GDP Grwoth by Countries by Using Pandas &amp; Folium Libs


What will you cover in this file (project) ?
Gather data from wikipedia.org List of countries by past and projected GDP using pandas.
First get the data and merge the correct tables together.
Next step is using Machine Learning with Linear regression model to estimate the growth of each country GDP.
Final step is to visualize the growth rates on a leaflet map using folium.

Step 1: Get the data and merge it
The data is available on wikipedia on List of countries by past and projected GDP. We will focus on data from 1970 to 2026.

At first glance on the page you notice that the date is not gathered in one table.

The first task will be to merge the three tables with the data from 1970-1979, 1980-1989, 1990-1999, 2000-2009, 2010-2019, and 2020-2026.

The data can be collected by pandas read_html function.

Step 2: Use linear regression to estimate the growth over the last 30 years
In this section we will use Linear regression from the scikit-learn library, which is a simple prediction tool.

Which shows that the model approximates a line through the 30 years of data to estimate the growth of the country’s GDP.

Notice that we use the product (cumprod) of pct_change to be able to compare the data. If we used the data directly, we would not be possible to compare it.

We will do that for all countries to get a view of the growth. We are using the coefficient of the line, which indicates the growth rate.

Step 3: Merge the data to a leaflet map using folium
The last step is to merge the data together with the leaflet map using the folium library.

There is a twist in the way it is done. Instead of using a linear model to represent the growth rate on the map, we chose to add them in categories. The reason is that otherwise most countries group in small segment.

Here we have used the qcut to add them in each equal sized group.

This should result in an interactive html page looking something like this.

