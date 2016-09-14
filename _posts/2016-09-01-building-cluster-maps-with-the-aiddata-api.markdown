---
title: Building Cluster Maps with the AidData API
date: 2016-09-01 08:13:00 -04:00
published: false
Author: John DeRiggi
---

![aiddataclient.PNG](/uploads/aiddataclient.PNG)
[Click Here to Open the AidData Client](http://daiblogviz.s3-website-us-east-1.amazonaws.com/)

[AidData](http://aiddata.org/) is an awesome organization. They've built a lightning fast API that exposes a massive amount of structured data about aid finances, projects, locations, and sources of funding.  More broadly and quoted from their Twitter bio, AidData is "a research and innovation lab based at William and Mary providing tools and services to make development finance more transparent and effective."

To scratch the surface of this great API, we built a super simple data explorer for the location-enabled project data. With some more work we hope it will help us investigate past projects in areas where we work. The app is a little rough around the edges but we want to share it and upgrade it over the next few months.

To use it just type in a country name into the search box and click around the map markers to see more details.
<!--more-->

**[Click Here to Open the AidData Client](http://daiblogviz.s3-website-us-east-1.amazonaws.com/)**

We are only using a tiny fraction of the available data from the API in this app. When you enter a country into the search box, the app requests the location-tagged project data for the country you searched for. Many projects will not show in this response as AidData can only collect data that is easily available.

Some of the project responses contain very little data, others contain lengthy text descriptions. You're likely to find both as you click around the markers.

As for the technical details, this is a super simple web app that runs completely in the browser. It uses an old-fashioned map layer from MapBox and some basic JavaScript for the API calls. We'll put it in a proper open source repository once we've cleaned it up a little that will help us consider new features for the application.
