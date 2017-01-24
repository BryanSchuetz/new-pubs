---
title: 'Remote Sensing Part 3: Identify Healthy Vegetation From Space, Without Leaving
  Your Desk.'
date: 2017-01-23 17:37:00 -05:00
published: false
tags:
- Remote Sensing Series
Author: John DeRiggi
---

DAI's excitement about the upcoming [SatSummit](https://satsummit.io/) is approaching perigee levels, with the conference less than one week away! This is part 3. Others: [part 2](https://dai-global-digital.com/part-2-la-la-landsat-making-use-of-landsat-imagery.html) and [part 1](https://dai-global-digital.com/remote-sensing-of-the-earth.html)


You could live a perfectly fulfilled life while taking for granted all the colors that appear in nature. However, when you ask "why?", doing so usually reveals a new fascinating level of complexity, and this is especially true for the color of things. The spectrum of visible colors, approximately, but not exclusively: red, orange, yellow, green, indigo, blue, and violet, are emitted from the sun along with all the invisible parts of the spectrum. Pure snow, (not that grey stuff that piles up at the parking lot at Walmart) is a brilliant bright white. You may recall having to wear sunglasses when the sun is out after a fresh snowfall because of the bright reflective white stuff layering the ground. **But why?** This is because snow reflects nearly all of the visible spectrum back to your eye, hence the white color. It has what remote sensing people call, high [albedo](https://en.wikipedia.org/wiki/Albedo).

Healthy leaves of basil are a luscious green color. **But why?** Plants absorb, rather than reflect, most of the red and blue light that hits the leaves. Absorption of light after all is part of the process of photosynthesis. It is also why trees are so vital to helping cool our planet - they absorb the energy from the sun instead of reflecting it back into our atmosphere. All of that results in basil leaves being deep green instead of white. 


![sunbeamingdownlight.jpg](/uploads/sunbeamingdownlight.jpg)
```The sun sends a full spectrum of light visible and invisible wavelengths of light to earth```

![sunbeamsdownandreflects-028a2d.jpg](/uploads/sunbeamsdownandreflects-028a2d.jpg)
```Healthy vegetation absorbs he red and blue light for photosynthesis. Some of the green light and high percentage of the short wave infrared light is reflected off the leaves```

What we don't see however is that healthy plants actually reflect more near infrared (short wavelength infrared) than visible green. That's right, plant's one could say are more infrared than they are green. But we humans only see the green. When a plant becomes unhealthy, it reflects more of the visible red light and less of the invisible infrared. Think of a dry plant that needs watering, it might turn a reddish brown color as it dries up. This difference between the visible red and the invisible near infrared light is a good measure of plant health. The bigger difference between the two, the healthier the plant. 

# An Index for Measuring Vegetation Health

To calculate the proportional difference in infrared light and visible red light, we can use the tried and true Normalized Difference Vegetation Index, or NDVI.

`NDVI = (NIR - RED) / (NIR + RED)`

Where NIR is near infrared and RED is visible red. If you're the type to gloss over equations, this one is simple! First off, this is just a ratio. In the case of NDVI it is the ratio of the elements` difference to it's sum. When the plant is really healthy it is reflecting a ton of NIR and very little RED. The range then for NDVI then is +1 to -1.

# An Example From Western Nepal
DAI Implements an Integrated Watershed Management Project for USAID called PANI. We can use an area of the western region, where PANI operates to study the vegetation health with NDVI at two different times of the year: August 2016 just after the monsoons, and January 2017: a dry and cold period in Nepal's weather pattern.

![nepalMapWithStudyArea.jpg](/uploads/nepalMapWithStudyArea.jpg)
```Our study area in wesern Nepal```

Let's look at a true color image of an area where our PANI project operates in western Nepal. You can see a few clouds and a river flowing full. This is from August of 2016 just after the monsoons.

![true_color_August_2016.JPG](/uploads/true_color_August_2016.JPG)
``` A true color image in western Nepal in August 2016 soon after the monsoon season. Notice the fat river```

To calculate the NDVI I can use QGIS (a free desktop GIS) and open up the raster calculator to run the formula with the red band (4) and the short wave infrared band (5). To do this go to Raster > Raster Calculator and type in the equation into the calculator. Here are a few images from the NDVI calcaulations. We can see a broader area of healthy vegetation afer the monsoons in August. Then later in January of the following year, the only healthy vegetation are in the select areas being irrigated by local farmers, the lowland forest and the mountain areas have begun to dry out.

![august_2016.JPG](/uploads/august_2016.JPG)
```NDVI just after the monsoon season in August 2016. On the ground we see a fairly even distribution of healthy green vegetation. The bright yellow blotches are clouds are scattered about in the scene```

![january_2017.JPG](/uploads/january_2017.JPG)
```NDVI for a dry day in early January 2017. We see healthy vegetation only in the irrigated farmland with the mountains and natural forest region drying out```

That's very satisfying to be able to see a change's in weather refleced in satellite imagery. Whats more, we did this all with free software and free imagery! We're looking forwarding to relying on Landsat and NDVI to help share with the community in Nepal the freely available ways to monitor watershed health.