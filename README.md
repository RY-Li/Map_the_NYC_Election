# map-nyc-election

<h2>Map the NYC 2025 Primary & General Mayoral Election<br>- Open-Source NYC Mayoral Real-Time Election Night Results Mapping at the Election District (ED) Level</h2>

<h3>About</h3>

This project provided an open-source pipeline and interactive maps that publish real-time election night results from the 2025 NYC mayoral primary and general election at the most granular Election District (ED) level.

Newsrooms and many institutions release polished maps, but the underlying data and code are usually closed. That makes it hard for students, journalists, and community groups to verify results, join their own data, or try new analyses. This project fixes that by putting everything—scrapers, processing scripts, and the map—on GitHub under a permissive license.


<br>


<h3>1). The <i>"general-mayoral-enr/2025-general.ipynb"</i> file:</h3>

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


<br>


<h3>2). The <i>"primary-mayoral-enr-web-archive/2025-primary-web-archive.ipynb"</i> file:</h3>

Similar to&nbsp;&nbsp;<i>"general-mayoral-enr/2025-general.ipynb"</i>&nbsp;, except used Web Archive (Wayback Machine - Internet Archive https://web.archive.org/) to retrieve the primary election data.


<br>


<h3>3). The <i>"primary-vs-general-mayoral-enr/2025-primary-vs-general.ipynb"</i> file:</h3>

Create a side-by-side map comparing <b>primary and general election results</b> for <b>Mamdani versus Cuomo</b> to visualize spatial shifts for the same top candidates.
<br>
<br>
<b>Go to https://r-li.com/Map_the_NYC_Election to view the map.</b>
<br>
<br>
<h3>Preview</h3>
<img src="pics/1.png" alt="Preview 1">
<br>
<img src="pics/2.png" alt="Preview 2">


<br>

<b>Contact me at 42@r-li.com for any question.</b>
