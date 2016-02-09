---
title: Open Data! Parcel Boundaries of Northern Afghanistan
date: 2016-01-18 19:46:00 Z
categories:
- open-data
tags:
- Afghanistan
Author: John Deriggi
---

![Parcel Boundaries 1.jpg](/uploads/afghanparcelstitle.png)

The USAID-funded RAMP UP North’s objective was to strengthen municipal governments in the northern part of Afghanistan. The principal component of this effort involved using a land management system to help government officials provide better services for their municipalities. The data presented here is the output of the geographic information system (GIS) analysts’ work to demarcate the boundaries of every parcel of property in the municipalities

<!--more-->

The data was traced using ArcGIS 10.1 and imagery from USAID’s GeoCenter. An effort was made to check data quality pertaining to gaps between adjacent boundaries but some gaps may still exist.

**Shapefile Downloads**
*Separate shapefiles for each municipality are available here. Each file uses the EPSG:4326 projection.*

|  Municipality  | Num Parcels | Download |
|:--------------:|:-----------:|:--------:|
|    Faizabad    |    11972    | [download ](https://drive.google.com/file/d/0B9Y8IICmeFgpb0xsNkZnZ1h5VDg/view?usp=sharing)|
|   Pul-e Kumri  |    24248    | [download ](https://drive.google.com/file/d/0B9Y8IICmeFgpOWxjWjhfTlJIQUE/view?usp=sharing)|
|      Khulm     |     7925    | [download ](https://github.com/deriggi/RAMPUPNorthData/blob/master/municipal_parcels_export/Balkh)|
| Mazar-e Sharif |    79865    | [download ](https://github.com/deriggi/RAMPUPNorthData/blob/master/municipal_parcels_export/Balkh)|
|     Andkhoy    |     9657    | [download ](https://github.com/deriggi/RAMPUPNorthData/blob/master/municipal_parcels_export/Faryab)|
|     Maymana    |    13740    | [download ](https://github.com/deriggi/RAMPUPNorthData/blob/master/municipal_parcels_export/Faryab)|
|   Sheberghan   |    24823    | [download ](https://github.com/deriggi/RAMPUPNorthData/blob/master/municipal_parcels_export/Jawzjan)|
|     Kunduz     |    31531    | [download ](https://github.com/deriggi/RAMPUPNorthData/blob/master/municipal_parcels_export/Kunduz)|
|      Aybak     |     5210    | [download ](https://github.com/deriggi/RAMPUPNorthData/blob/master/municipal_parcels_export/Samangan)|
|    Sar-e Pul   |     9685    | [download ](https://github.com/deriggi/RAMPUPNorthData/blob/master/municipal_parcels_export/Sarepul)|


## The Uses of Parcel Boundaries
The parcel data is applicable to a variety of situations and is probably most valuable to Afghan municipal governments and data practitioners working in Afghanistan. Hopefully, the people of Afghanistan can use the data to simply study and improve the urban areas near where they live.

The data is especially relevant to the field of disaster response. Northern Afghanistan has a [history of earthquakes](http://earthquake.usgs.gov/earthquakes/world/historical_country.php#afghanistan), including two in 1998 in which more than 6,000 people lost their lives. With the danger clearly there, accurate urban spatial data could help people plan and respond to natural hazard events in the future.

After the Haiti earthquake, there was a conspicuous lack of spatial data about building infrastructure. This resulted in an [an incredibly fast construction](http://vimeo.com/9182869) of open spatial data in OSM. Presumably, if first responders had access to this data before the earthquake then the relief effort could have been more efficient.

## Working with the data

The easiest way to work with the data is to open it up in your favorite GIS. QGIS is a free tool and works well for analyzing shapefiles. [Download QGIS](http://www.qgis.org/en/site/forusers/download.html) if you do not already have it on your machine:

* Choose one of the files from the table above and download it and unzip it
* Open up QGIS
* Drag the .shp file onto your workspace 

![Parcel Boundaries 2.jpg](/uploads/Parcel Boundaries 2.jpg)

## A Web Map of the Mazar-e Sharif Data

[Interact with the Mazar-e Sharif Data
](http://deriggi.github.io/RUNorthArcPy/mazar/mazar.html)

## Sample Visualizations

Here some sample visualizations to give you an idea of the how the municipalities vary in size and distribution. Each was made with QGIS.

**Mazar-e Sharif**
![Parcel Boundaries 3.jpg](/uploads/Parcel Boundaries 3.jpg)
**Faizabad**
![Parcel Boundaries 4.jpg](/uploads/Parcel Boundaries 4.jpg)
**Pulekhumri**
![Parcel Boundaries 5.jpg](/uploads/Parcel Boundaries 5.jpg)
**Khulm**
![Parcel Boundaries 6.jpg](/uploads/Parcel Boundaries 6.jpg)
**Maymana**
![Parcel Boundaries 7.jpg](/uploads/Parcel Boundaries 7.jpg)
**Shberghan**
![Parcel Boundaries 8.jpg](/uploads/Parcel Boundaries 8.jpg)
**Kunduz**
![Parcel Boundaries 9.jpg](/uploads/Parcel Boundaries 9.jpg)