---
title: 'Part 2: La La Landsat. Accessing Landsat Imagery'
date: 2017-01-17 12:11:00 -05:00
published: false
---

*DAI is in a stellar mood about the upcoming [SatSummit](https://satsummit.io/) in Washington D.C.* 
<!-- more -->

Some incredible things were happening in the U.S in 1972: Bill Withers Lean on Me was the number one song, the first Godfather film was released, and NASA launched the first in a series of satellites designed to provide consistent and reliable coverage of the earth’s land cover. The platform, called the Earth Resources Technology Satellite or ERTS-1 was developed in partnership with USGS, who agreed to handle the storage and archiving and distribution of the data products. The second satellite, eventually renamed Landsat 2 launched in 1975, operating in parallel with ERTS-1 for a few years unti the original satellite was decommissioned in 1978.
 
In the late 1980s, the program hit hard times, reporting few users of the data, and scrutiny from congress. It was saved only through direct intervention from Vice President Dan Quayle, who perhaps should be remembered more for saving Landsat than an unfortunate incident with a chalkboard and a root vegetable. 

Today, Landsat8 and Landsat 7 are operating concurrently. Here is the mission schedule from USGS

![TimelineOnlyForWebRGB.jpg](/uploads/TimelineOnlyForWebRGB.jpg)
``` Landsat Mission schedule. Image credit: USGS```

Landsat data is free to the public. To get access to this treasure trove you can go through the traditional [USGS Earth Explorer Site](https://earthexplorer.usgs.gov/).   This is one of the main publicly operated distribution sites for Landsat data (and quite a few other programs). To get at the data, you simply select the point or area of interest and then click a button to query for all possible results. After selecting the imagery product you want to see, you can select a preview of the image to get a sense for the footprint. Here is a scene just west of Madison Wisconsin.

![wisconsinusgs.png](/uploads/wisconsinusgs.png)
``` A screenshot from the Earth Explorer Site ```

As a registered user, when you download a scene you get the full stack of 11 bands plus the Quality Assessment Band which is an imagery layer that describes characteristics of the scene based on cloud cover, the presence of snow or ice, and several other indicators that could alter numeric calculations of the image.

As an alternative, Amazon Web Services [hosts Landsat8 data](C:\Users\jderiggi\Downloads\For more information about Landsat on AWS) since 2015 and you can easily download the data once you know the scene number, by reconstructing it as a URL. Here is a [scene from the DRC](http://landsat-pds.s3.amazonaws.com/L8/173/061/LC81730612016171LGN00/index.html)

So what do you do with this data? Now you can construct false color images by layering together the bands. So, if you want to create a 5-4-3 image you need to combine layers (you guessed it) 5, 4, and 3. In QGIS, the free desktop GIS tool, you can combine these. In QGIS, simply select Raster > Miscellaneous > Build Virtual Raster to combine the three layers into one. This [MapBox blogpost](https://www.mapbox.com/blog/putting-landsat-8-bands-to-work/) from 2013 has a great description of the color combinations that would be of interest.
 
# Other Landsat Tools
This humble site from the good people at wisconsinview.org is great because it shows the most recent orital tracks for Landsat8. This gives you a good view of the polar orbit (Landsat crosses the poles on every orbt) and also for the distortion in the projection at the northern and southern latitudes. You can see the fattening of the images aroudn Canada and Antartica. Right clicking on a scene shows presents some raw data and also a two options for downloading. One on the EarthExplorer site and another on AWS, Amazon Web Services. [Check it out!](http://wisconsinview.org/imagery/viewer.php?products=lsat8-llook-fc,wrs2-land.-44&timespan=-16d,-1d&timestep=1d)

Landsat Live from Mapbox is a viewer that shows landsat images tiled across the earth with helpful attribute data for each image. Here is a look at a [scene from Dubai](https://www.mapbox.com/bites/00145/#11/25.0411/55.3546)

We hope this peaks your interest in Landsat and helps you see how easy it is to start using the imagery to advance your project's work.
