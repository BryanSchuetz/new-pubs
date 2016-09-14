---
title: Building Cluster Maps with the AidData API
date: 2016-09-01 08:13:00 -04:00
published: false
---

[AidData](http://aiddata.org/) is an awesome organization. They've built a lightning fast API that exposes a massive amount of structured data about aid finances, projects, locations, and sources of funding.  More broadly and quoted from their [Twitter bio](https://twitter.com/aiddata?lang=en), AidData is "a research and innovation lab based at William and Mary providing tools and services to make development finance more transparent and effective."

We built a super simple data explorer for GIS elements within the AidData API to help us explore past projects in specific countries. The app is a little rough around the edges but we want to share it and upgrade it over the next few months

<!--more-->

**[Click Here to Open the AidData Client](http://daiblogviz.s3-website-us-east-1.amazonaws.com/)**

This is a super simple web app that runs completely in the browser. Some of the project responses contain very little data, others contain lengthy text descriptions. You're likely to find both as you click around the markers.

This app uses an old-fashioned map layer from MapBox and some simple JavaScript for the API calls. We'll put it in a proper open source repository once we've cleaned it up a little.  

