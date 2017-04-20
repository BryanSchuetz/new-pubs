---
title: First Contact with the Planet API and NodeJS
date: 2017-04-20 09:36:00 -04:00
published: false
---

![thumbnails-054255.png](/uploads/thumbnails-054255.png)
``` Thumbnails of Sentinel Imagery from Planet's API```
We love remote sensing here at DAI and satellite imagery API's are starting to pop up all over, like springtime flowers in DC. [Planet ](https://www.planet.com/)is a relatively small company with lofty service and product offerings. Specifically, they build and launch small satellites that image the entire world every day, they provide access to the imagery through a web platform, and they give developers access to their core data through a web API.

We love [APIs](https://en.wikipedia.org/wiki/Application_programming_interface) here at DAI and we're really excited about the prospect of building some custom apps to collect imagery for some of our project sites. The [API docs](https://www.planet.com/docs/) for Planet are thorough enough that you can derive how to interact with the API in the programming language of your choice. They have a few Python examples on the site but none for NodeJS in the latest version of the API. 

One of the apps we're cooking up here at DAI is something that helps us monitor locations based on a few configurable parameters. In the following code block, we have a NodeJS script that makes an authenticated request for recent Sentinel imagery that was acquired any time since January 1st 2017, has downloadable assets, and is an image with at least 85% viable data. Some images are only slices of a complete tile so we want to specify what is referred to as a minimum threshold for black-fill.

If you want to use the code you first need to [register as a developer with Planet](https://www.planet.com/explorer/) and get your API key. That is the only thing you need to change in the code before running it on your own machine.

# Making a Request to the API
Here's the code to make a request to the Planet API using NodeJS

<script src="https://gist.github.com/deriggi/3ad1186b460b3587adbbfabbac83d9c7.js"></script>

# Reading the Response
Our response comes back as a pageable list of responses with 250 records in each page! 
<script src="https://gist.github.com/deriggi/e6bc26063e72dcc53b2cbd25f3771ce1.js"></script>
 