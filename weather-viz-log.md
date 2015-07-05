# Bozeman Weather vizualization documentation

Goal: To create a weather chart for Bozeman modeled after the [2004 NY City weather chart](http://www.edwardtufte.com/bboard/q-and-a-fetch-msg?msg_id=00014g) highlighted by Edward Tufte.

Also want to add rainfall data by day (maybe compare to typical cumulative rainfall)

## Data needed 

For each day:
- Record high temp
- Record low temp
- Average high temp
- Average low temp
- Recorded high temp
- Recorded low temp
- Recorded precipitation
- Typical precipitation? (makes more sense to display this as cumulative)


## Resource links

[National Weather Service info page](http://www.weather.gov/help-past-weather)

[Great Falls, MT National Weather Service Station](http://www.wrh.noaa.gov/tfx/) (spans Bozeman)

[Weather station w/ complete Bozeman coverage](http://www.ncdc.noaa.gov/cdo-web/datasets/GHCND/stations/GHCND:USC00241044/detail) - Looks like MSU campus station

[Data source for some MT cities - not Bozeman](http://academic.udayton.edu/kissock/http/Weather/citylistUS.htm)

## Viz components

Weather banding
For each day: 
- Rectangle for record high/low
- Rectangle for average high/low
- Rectangle for specific year high/low

Axis on weather bands
- Temperature scale (increments of 10 degrees Farenheit) - both sides of graph
- Horizontal banding at 10 degree increments
- Special band at 32 F / freezing
- Month labels
- Vertical bars separating months

Legend
- Record high / low bar + labels
- Normal range high / low bar + labels
- Actual high / low bar + labels

Precipitation stuff
- Figure out how to display this

Call outs on record highs/lows?

## Work log

Data obtained from NOAA 

Working off 2014 data to start with

Used csvkit.csvcut to truncate data
csvcut -c 6,7,10,11 BZN-weather-data_2014.csv > bzn-weather-2014-clean.csv
https://csvkit.readthedocs.org/en/0.9.1/scripts/csvcut.html

Started with Mike Bostock bar chart d3 example

As of 6/4/15, had daily high/low for 2014 sketched out

