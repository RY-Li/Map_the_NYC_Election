# map-nyc-election

<h2>Map the NYC 2025 Primary & General Mayoral Election<br>- Open-Source NYC Mayoral Real-Time Election Night Results Mapping at the Election District (ED) Level</h2>

<h3>About</h3>

This project offers an open-source pipeline and interactive maps that publish real-time election night results from the 2025 NYC primary and general mayoral election at the most detailed Election District (ED) level.

Newsrooms and many institutions release polished maps, but the underlying data and code are often not openly available. This makes it hard for students, journalists, and community groups to verify results, integrate their own data, or explore new analyses. This project addresses that by making everything—scrapers, processing scripts, and the map—available on GitHub under a permissive license.

The pipeline extracts data from the NYC Board of Elections ENR (Election Night Results) tables in HTML, standardizes candidate fields across party lines, calculates ED-level totals and percentages, and exports tidy CSV files. It then joins results with the NYC Department of City Planning's clipped ED boundary data to create a GeoPackage, enabling direct use in GIS tools. The accompanying web map provides precinct-level tooltips and easy downloads so others can combine results with open data sets (Census, housing, transit, environmental layers) and explore their own questions. The scripts are designed to be future-proof so that they can be reused for future elections—users simply need to change the election ID.

Since <b>Zohran Mamdani</b> and <b>Andrew Cuomo</b> were the top two candidates in both the <b>Democratic primary</b> and the <b>general</b> mayoral election, maps were created to illustrate spatial continuity and to compare changes in election results as examples of this pipeline's capabilities. This project applied the same pipeline to both races to produce the map titled "<b>Map the Election: Mamdani vs. Cuomo - Primary vs. General</b>," which displays shifts in support side-by-side. An additional map, titled "<b>Primary to General Election Two-Way Vote Share Shift in Percentage Points</b>," was generated through analysis to quantify the voting changes. Subway routes were also added to the maps as an optional reference layer.

The goal is simple: to make high-resolution election data accessible and remixable so more people can conduct independent, transparent analyses.


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

To visualize spatial shifts for the same top candidates for the primary and general election:
1. Create a side-by-side map comparing <b>primary versus general election results</b> for <b>Mamdani and Cuomo</b>
2. Create a map for <b>two-way vote shift from primary to general election</b> in percentage points for <b>Mamdani and Cuomo</b>
3. Add <b>subway routes</b> to the maps as a reference (did you find some patterns?)
<br>
<br>
<b>Go to https://r-li.com/map-nyc-election to view the map.</b>
<br>
<br>
<h3>Maps Preview</h3>
<h4>Primary vs. General</h4>
<img src="readme_pics/1.png" alt="Preview 1">
<br>
<img src="readme_pics/2.png" alt="Preview 2">
<br>
<img src="readme_pics/3.png" alt="Preview 3">
<h4>Vote Shift</h4>
<img src="readme_pics/4.png" alt="Preview 4">
<br>
<img src="readme_pics/5.png" alt="Preview 5">
<br>
<img src="readme_pics/6.png" alt="Preview 6">



<br>

<b>Contact me at 42@r-li.com for any question.</b>
