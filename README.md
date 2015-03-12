# Earthquake Frequency Analysis and Maps

*Quick link: [See the analysis](http://nbviewer.ipython.org/github/buzzfeednews/2015-03-earthquake-maps/blob/master/notebooks/earthquake-state-analysis.ipynb).*

This repository contains:

- Data and code used to analyze the decade-over-decade percentage change in earthquake frequency in each state in the United States.
- Code to create SVG maps of earthquakes in four states:  Arkansas, Kansas, Oklahoma, and Texas.

The analysis and maps are referenced in the March 6, 2015 BuzzFeed News article, "[Midwestern States Are Having Big Earthquakes Like Never Before](http://www.buzzfeed.com/danvergano/midwestern-states-are-having-big-earthquakes-like-never-befo)."

## Data

The [data/earthquake_states.csv](data/earthquake_states.csv) file contains information about all earthquakes of magnitude three or greater detected in the United States from 1975 through February 2015. The data were obtained via the [U.S. Geological Survey](http://earthquake.usgs.gov/earthquakes/search/) and preprocessed in [PostGIS](http://postgis.net/) to match each quake to the state containing its epicenter.

The [stateshapes](data/stateshapes/) directory contains shapefiles for Arkansas, Kansas, Oklahoma, and Texas, [obtained from the U.S. Census Bureau](https://www.census.gov/cgi-bin/geo/shapefiles2010/main).

## Analysis

Analysis for this project was conducted in an IPython notebook, the raw version of which can be found [here](notebooks/earthquake-state-analysis.ipynb). A rendered version of the notebook, which doesn't require installing or running any software, can be [viewed here](http://nbviewer.ipython.org/github/buzzfeednews/2015-03-earthquake-maps/blob/master/notebooks/earthquake-state-analysis.ipynb).

The maps were also generated in an IPython notebook, the raw version of which can be found [here](notebooks/make-state-maps.ipynb).

## Output

The code in [notebooks/make-state-maps.ipynb](notebooks/make-state-maps.ipynb) saves SVG maps to the [output](output) directory. There are two maps for each state: a "before" map, which contains all earthquakes of magnitude three or greater in the state between 1995-2004, and an "after" map, which contains all earthquakes of magnitude three or greater in the state between 2005-2014.
