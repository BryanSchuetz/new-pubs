---
title: First Contact with the Planet API and NodeJS
date: 2017-04-20 09:36:00 -04:00
published: false
---

![thumbnails.png](/uploads/thumbnails.png)
``` Thumbnails of Sentinel Imagery from Planet's API```
We love remote sensing here at DAI and the new imagery API's are popping up all like springtime flowers in DC. Planet is a relatively small but lofty company that does many things: They build and launch small satellites that image the entire world every day, they provide access to the imagery through a web platform, and they provide access to their core data through an API.

We love APIs here at DAI and we're really excited about the prospect of building some custom apps to collect imagery for each of our project sites. The API docs for Planet are thorough enough that you can derive how to interact with the API in the language of your choice. They have a few Python examples on the site but none for NodeJS on the latest version of the API. 

One of the apps we're cooking up here at DAI is something that helps us monitor locations based on a few configurable parameters. In the following code block, we have a NodeJS script that makes an authenticated request for recent Sentinel imagery that was acquired any time since January 1st 2017, has downloadable assets, and is an image with at least 85% viable data. Some images are only slices of a complete tile so we want to specify what is referred to as a minimum threshold for black-fill.

Here's the code!

<script src="https://gist.github.com/deriggi/3ad1186b460b3587adbbfabbac83d9c7.js"></script>
 