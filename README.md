# 2015-03 Earthquake Maps

*Quick link: [See the analysis](http://nbviewer.ipython.org/github/buzzfeednews/2015-03-earthquake-maps/blob/master/notebooks/earthquake-state-analysis.ipynb).*

This repository contains the data and code used to analyze the decade-over-decade percentage change in earthquake frequency in each state in the United States. It also contains the code to create SVG maps of earthquake events. This analysis is referenced in the March 6, 2015 BuzzFeed News article, "[Midwestern States Are Having Big Earthquakes Like Never Before](http://www.buzzfeed.com/danvergano/midwestern-states-are-having-big-earthquakes-like-never-befo)."

## Data

The USGS provides the ability to search for earthquake events in its online tool. Because the USGS data includes both latitude and longitude along with a location that's not exactly a state, the data was then run through a postGIS database to determine in which state the center of the earthquake was located. The calculated state is named "state" in the CSV.

- [All earthquakes of magnitude three or greater from 1975 through February 2015](https://github.com/BuzzFeedNews/2015-03-earthquake-maps/blob/master/data/earthquake_states.csv?raw=true)

In order to make the earthquake maps you need state shapefiles. These were downloaded from the U.S. Census:

- stateshapes directory including: arkansas, kansas, oklahoma, and texas

## Analysis

Analysis for this project was conducted in an IPython notebook, the raw version of which can be found [here](notebooks/earthquake-state-analysis.ipynb). A rendered version of the notebook, which doesn't require installing or running any software, can be [viewed here](http://nbviewer.ipython.org/github/buzzfeednews/2015-03-earthquake-maps/blob/master/notebooks/earthquake-state-analysis.ipynb). The generation of the maps was also done in an IPython notebook, the raw version of which can be found [here](notebooks/make-state-maps.ipynb).

## Output

The code in the make-state-maps notebook generates SVG maps to this directory. There are two maps for each state a "before", which contains all earthquakes of magnitude three or greater in the state between 1995-2004, and an "after" which contains all earthquakes of magnitude three or greater in the state between 2005-2014.