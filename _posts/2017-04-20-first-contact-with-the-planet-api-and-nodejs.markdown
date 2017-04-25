---
title: First Contact with the Planet API and NodeJS
date: 2017-04-20 09:36:00 -04:00
published: false
tags:
- Remote Sensing Series
- Data
Author: John DeRiggi
---

![thumbnails-054255.png](/uploads/thumbnails-054255.png)
``` Thumbnails of Sentinel Imagery from Planet's API```
We love remote sensing here at DAI and luckily for us, satellite imagery APIs are starting to pop up all over, like springtime flowers in DC. One of the most prominent imagery providers is [Planet](https://www.planet.com/), a small company with lofty service and product offerings for remote sensing. Planet builds and launches small satellites that image the entire world every day. They provide access to imagery through a web platform, and they give developers access to their data through a web API.

We're really excited about the prospect of building custom apps to collect imagery for some of our project sites. The [API docs](https://www.planet.com/docs/) for Planet are thorough, letting you work out how to write a client of the API in the programming language of your choice. They have a few Python examples on the site but none for NodeJS in the latest version of the API - so let's make one! 

<!--more-->

One of the apps we're cooking up here at DAI is one that helps us monitor a work site with regularly updated satellite imagery. In the following code block, we have a NodeJS script that makes an authenticated request for recent Sentinel imagery products that meet the following criteria: covers an area near Malibu, California, acquired any time since January 1st 2017, has downloadable assets, is an image with at least 85% actual imagery data data. The reason for that last criterion is that some images are only slices of a complete tile, so we want to specify a minimum threshold for imagery data per tile, something referred to as [blackfill](https://www.planet.com/docs/glossary/) in the Planet glossary.  

# Making a Request to the API
Here's the code to make a request to the Planet API using NodeJS. If you want to use the code, you first need to [register as a developer with Planet](https://www.planet.com/explorer/) to get your API key, and then insert it on line 76. That is the only change you need to make in the code before running it on your own machine.

<script src="https://gist.github.com/deriggi/3ad1186b460b3587adbbfabbac83d9c7.js"></script>

# Reading the Response
Our response comes back as a page-able list of responses with 250 records in each page, with each record corresponding to a single imagery product. One record contains the coordinates for the perimeter of the tile, as well as a long list of useful parameters like cloud cover, sun angle, and image source. To actually download the imagery you need to make another authenticated web request using the asset link that is part of each response object. 
<script src="https://gist.github.com/deriggi/e6bc26063e72dcc53b2cbd25f3771ce1.js"></script>

![malibu_3-215f3c.png](/uploads/malibu_3-215f3c.png)
```Thumbnails in the response of our API request for images near Malibu, CA```
This is a super-simple start, just scratching the surface of the API but we hope you find ways to use it in your work.
 