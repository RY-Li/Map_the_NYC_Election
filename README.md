# Map_the_NYC_Election

<h2>Map the NYC 2025 General Election<br>- Open-Source NYC Mayoral Election Night Real-Time Results Mapping at the Election District (ED) Level</h2>

<h3>About</h3>

This project provided an open-source pipeline and an interactive map that publishes the election night real-time results from the 2025 NYC mayoral general election at the most granular Election District (ED) level.

Newsrooms and many institutions release polished maps, but the underlying data and code are usually closed. That makes it hard for students, journalists, and community groups to verify results, join their own data, or try new analyses. This project fixes that by putting everything—scrapers, processing scripts, and the map—on GitHub under a permissive license.



<h3>The "NYC 2025 General Election.ipynb" file</h3>

<b>PART 1: NYC Mayoral ENR scrape</b>

1. Pull the NYC Board of Elections ENR (Election Night Results) tables, and export the orgional result to a single CSV file. 
2. Sstandardize candidate fields across party lines, calculate ED-level totals and percentages, and export tidy CSV.
3. Join results to the NYC Department of City Planning's clipped ED boundaries to generate a GeoDataFrame, and export to another CSV and a GeoPackage so the data drops straight into GIS tools.

Users of this GeoPackage file can combine the results with open data (e.g. Census, housing, transit, environmental layers) and ask their own questions.

The scraper are also future-proof so that they will work the same for future elections—the user can make them work by just changing the election ID (and the ED boundary release version if appliable). 


<b>PART 2: Map the Result</b>

1. Map 1: Mamdani Only
2. Map 2: Mamdani vs. Cuomo: new GeoDataFrame generated to include the winner for each ED and their winning percenrage
3. Export the GeoDataFrame to CSV and GeoPackage, and export the interactive map to HTML.

Go to https://r-li.com/Map_the_NYC_Election to view the map.

<b>Contact me at 42@r-li.com for any questions.</b>
