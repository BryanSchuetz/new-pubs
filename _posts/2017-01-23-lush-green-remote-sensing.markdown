---
title: 'Remote Sensing Part 3: Identifying Healthy Vegetation From Space!'
date: 2017-01-23 17:37:00 -05:00
published: false
---

Bold statement alert: Basil is green and snow is white. Now, you could live a perfectly fulfilled life taking that for granted, along with all the other beautiful natural colors in the world. However, at DAI we like to ask, “But why?” because doing so ususally reveals a new fascinating level of complexity, and this is especially true for the color of things.

The spectrum of visible colors, approximately, but not exclusively: red, orange, yellow, green, indigo, blue, and violet, are emitted from the sun along with all the invisible parts of the spectrum. Pure snow, (not that grey stuff that piles up at the parking lot at Walmart) is a bright white. You may recall having to wear sunglasses when the sun is out after a fresh snowfall because of the bright reflective white stuff layering the ground. **But why?** This is because snow reflects nearly all of the visible spectrum back to your eye, hence the white color. It has what remote sensing people call, high [albedo](https://en.wikipedia.org/wiki/Albedo).

Healthy basil is a luscious green color. **But why?** Plants absorb, rather than reflect, most of the red and blue light that hits the leaves. Absorbtion of light is part of the process of photosynthesis. It is also why trees are so vital to helping cool our planet - they absorb the energy from the sun instead of reflecting it back into our atmosphere. All of that adds up to basil being green instead of white. What we don't see however is that healty plants actually reflect more near infrared (short wavelength infrared) than visible green. When a plant becomes unhealthy, it reflects more of the visible red light and less of the invisible infrared. This difference between the visible red and the invisible near infrared light is a good measure of plant health. 

![sunbeamingdownlight.jpg](/uploads/sunbeamingdownlight.jpg)
```The sun sends a full spectrum of light visible and invisible wavelengths of light to earth```

![sunbeamsdownandreflects-028a2d.jpg](/uploads/sunbeamsdownandreflects-028a2d.jpg)
```Healthy vegetation absorbs he red and blue light for photosynthesis. Some of the green light and high percentage of the short wave infrared light is reflected off the leaves```

# Vegetation Index

To calculate the proportional difference in infrared light and visible red light, we can use the tried and true Normalized Difference Vegetation Index, or NDVI.

`NDVI = (NIR - RED) / (NIR + RED)`

Where NIR is near infrared and RED is visible red. If you're the type to gloss over equations, don't! First off, this is just a simple ratio. In the case of NDVI it is the ratio of the elements difference to it's sum. When the plant is really healthy it is reflecting a ton of NIR and very little RED. The range then for NDVI is +1 to -1.

# An Example From Western Nepal

![nepalMapWithStudyArea.jpg](/uploads/nepalMapWithStudyArea.jpg)
```Our study area in wesern Nepal```

![true_color_August_2016.JPG](/uploads/true_color_August_2016.JPG)
``` A true color image in western Nepal in August 2016 soon after the monsoon season. Notice the fat river```

![august_2016.JPG](/uploads/august_2016.JPG)
```NDVI just after the monsoon season in August 2016. On the ground we see a fairly even distribution of healthy green vegetation. The bright yellow blotches are clouds are scattered about in the scene```

![january_2017.JPG](/uploads/january_2017.JPG)
```NDVI for a dry day in early January 2017. We see healthy vegetation only in the irrigated farmland with the mountains and natural forest region drying out```


