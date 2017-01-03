# Evapotranspiration Data Integration Need
Evapotranspiration measures the water needs of landscapes and forms a critical data point in Governor Brown's new long term framework for water conservation.  This data is measured statewide in geospatially sparse in situ sensor networks and interpolating that data across California requires wind, precipitation, solar radiation and other publicly available data.  Those data sources however are fragmented and integrating those together along with the appropriate scientific methodology can help improve this important measurement for the people of California.

## Current Evapotranspiration Data in California

The canonical source of evapotranspiration data for water managers in California is CIMIS. From the [CIMIS website](http://www.cimis.water.ca.gov/): 

>The California Irrigation Management Information System (CIMIS) is a program unit in the Water Use and Efficiency Branch, Division of Statewide Integrated Water Management, California Department of Water Resources (DWR) that manages a network of over 145 automated weather stations in California. CIMIS was developed in 1982 by DWR and the University of California, Davis (UC Davis). It was designed to assist irrigators in managing their water resources more efficiently. Efficient use of water resources benefits Californians by saving water, energy, and money.

The primary problem with these sensors is that they are far apart and located primarily in agricultural areas. To improve on this, DWR and UC Davis maintain a data set known as [Spatial CIMIS](http://www.cimis.water.ca.gov/):

>Most of the CIMIS stations produce estimates of reference evapotranspiration (ETo) for the station location and their immediate surroundings, often in agricultural areas. Because of California's diverse landmass and climate, many locations within the state lack a representative CIMIS station. Some counties, for example, do not have a CIMIS station and others have only one or two stations. As a result, there are significant spatial ETo data gaps, especially in urban areas. In an attempt to mitigate this problem, CIMIS initiated a study to investigate the possibility of coupling remotely sensed satellite data with point measurements from the CIMIS weather stations to generate spatially distributed ETo values (ETo maps).

## Opportunity for Improvement

Spatial CIMIS is valuable because it produces detailed maps of ETo on a 2km grid accross California.

![ET Map](http://spatialcimis.water.ca.gov/cimis/2016/07/14/et0.png)

However, under the current [Spatial CIMIS methodology](https://www.researchgate.net/publication/228669634_Daily_reference_evapotranspiration_for_California_using_satellite_imagery_and_weather_station_measurement_interpolation), only solar radiation values are measured in a grid accross the whole state (via sattelite imagery). The [other values needed to calculate ETo](http://hydrology1.nmsu.edu/pet/penman-montheith.pdf) are interpolated between point measurments at the sparse CIMIS stations. This can lead to inaccuracies in urban areas when attempting to measure ETo at the scale of water utility service areas or smaller.

## Hypothesis

The motivating hypothesis of this project is that the spatial resolution and/or accuracy of ETo measurements can be improved by making use of the wide variety of heterogeneous weather data that is now available online. This would increase the spatial density of available sensors and hopefully increase the sensitivity of ETo measurements to microclimates caused by natural physiography and human settlements.

# Potential Raw Data Sources to be Integrated
1. [Precipitation from CDEC](http://cdec.water.ca.gov/misc/RealPrecip.html)
2. Temperature
3. Wind
4. Land Cover (NAIP)
5. Physiography
6. [Forecasted ET from NOAA](http://www.wrh.noaa.gov/forecast/evap/FRET/FRET.php?wfo=sto)
  - [See here for technical documentation on the NOAA forecasted ET gridded data](https://www.google.com/url?q=http://ndfd.weather.gov/technical.htm&sa=D&ust=1483383177762000&usg=AFQjCNGG3mUFtYLThq6PzvMVS0Bui8tNlA)

# References

Hart, Q. J., Brugnach, M., Temesgen, B., Rueda, C., Ustin, S. L., & Frame, K. (2009). Daily reference evapotranspiration for California using satellite imagery and weather station measurement interpolation. Civil engineering and environmental systems, 26(1), 19-33.

Snyder, R. L. (2005). The ASCE standardized reference evapotranspiration equation. Technical Committee report to the Environmental and Water Resources Institute of the American Society of Civil Engineers from the Task Committee on Standardization of Reference Evapotranspiration, 173.
