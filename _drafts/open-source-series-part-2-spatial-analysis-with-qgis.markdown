---
title: 'Open Source Series Part 2: Spatial Analysis with QGIS'
date: 2017-08-21 10:46:00 -04:00
tags:
- GIS
- Data Visualization
- Web Mapping
Author: Greg Maly
social-image: "/uploads/QGIS%20new.jpg"
---

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSenKhci6-nWy6GVwj7ZXgGI4zq_7DAEbyaMhdbqqm_PNlVKxw/viewform?embedded=true" width="760" height="700" frameborder="0" marginheight="0" marginwidth="0">Loading...</iframe>

*In this article, we’ll explore the open source software package QGIS through a look at the history of the application, take a sneak peek into how the software functions, and then talk about how it compares to proprietary software applications – particularly when being used by development and diplomatic focused organizations.*

![QGIS new.jpg](/uploads/QGIS%20new.jpg)

There has been a buzz around the release of QGIS version 3.0 for a couple of years now. On a personal note - QGIS has been my go-to desktop GIS application for the past five years, so I was thrilled to receive an e-mail from the [QGIS LinkedIn user group](https://www.linkedin.com/groups/2290177) with a link to beta test QGIS 2.99, a pre-release copy of the version 3.0. No hesitation there, it was finally a time to give it a whirl.

## Part 1: What is QGIS?

[QGIS](http://www.qgis.org/), formerly known as Quantum GIS, is a powerful desktop software application that puts spatial analysis and cartographic capabilities in the hands of anyone with a computer capable of rendering large files, and the willingness to learn. It is arguably the most powerful open source desktop GIS available today, is currently translated into over 40 languages, and is backed by some very dedicated developers. QGIS version 0.0.1 was original developed and released by Gary Sherman in July 2002, and was adopted as an incubator projected of the [Open Source Geospatial Foundation](http://www.osgeo.org/) in 2007.  Version 1.0, Kore, was released in early 2009.

While I used the application throughout releases of version 1, Version 2.0, Dufour, is when I remember starting to rely on the software for every day GIS tasks. The application was capable of functions you could previously only expect to find in proprietary software. You can take a look at the change-logs [here](http://www.qgis.org/en/site/forusers/visualchangelog200/index.html), but that new release introduced smarter labeling functions, improved heatmaps, a visual process modelling function, new features for raster analysis, a layer panel that was easier to navigate, a better print composer, and much more. Each new release along the 2.x series brought improvements, and new converts to the QGIS world. So, what can we expect in Version 3.0?

Per the website [GeoGeek](https://geogeek.xyz/), QGIS 3.0 includes access to the newest version of Qt and Python, a higher quality user interface, improved geometry editing and processor dialogs, new symbols, better search functions within layers, custom image sizes, and support for 3D analysis. That’s a lot. But what does that mean in practice? Let’s have a look.

## Part 2: Putting QGIS 3.0 to the test

With full recognition that the software is still in BETA, I booted up version 2.99 to put some very basic functions to the test.

The first thing I noticed was a redesigned Data Source Manager toolbar. The data import and export function, which has always been one of QGIS’s greatest strengths, has been revamped. The software is prepared to ingest almost any kind of spatial data and database available today.

The first thing I did was load up the Admin0 global dataset from the [Global Administrative Areas website,](http://www.gadm.org/) and a .csv of child mortality rates by country over time from the [World Bank’s Open Data portal](http://data.worldbank.org/).  A quick glance at the Attributes Table view showed a very similar interface. The Field Calculator and sorting functions were all familiar. Not much changed here.

Opening the Layer Properties panel, I noticed a couple of new features, including a new “Information” page, improved access to meta data, and maybe most interestingly, a section on “Dependencies”, which enables the user to control how data sets interact when changes are made to the underlying data. I can see this being incredibly useful when joining multiple layers, or running spatial calculations across multiple layers.
![Data Source Manager.png](/uploads/Data%20Source%20Manager.png)

The next thing I looked at was the Processing Toolbox, which includes a host of analytical functions. This interface had been totally overhauled from version 2.18, and is arguably where the power of GIS begins. I won’t go into much detail on these functions here, but will just complement the design team on making the section much more inviting.

Back to the mapping…

I quickly joined the World Bank data to the Global Boundaries, created a [choropleth map](https://en.wikipedia.org/wiki/Choropleth_map) based on 2015 child mortality projections using Equal Intervals as the color ramp mode, and rendered the polygons as a sphere using the [Azimuthal Equidistant projection](https://en.wikipedia.org/wiki/Azimuthal_equidistant_projection).

The whole process took no more than an hour (including poking around at the new buttons), and rendered the following map, which displays child mortality rates (under age 5) per 1,000 live births.\
![Child Mortality Rates_2015.png](/uploads/Child%20Mortality%20Rates_2015.png)

While there may be a package or function that already accomplishes this, I’d like to highlight that the histogram included in the map is a screen grab from the Properties - > Symbology box. As we increasingly see data visualization software like Tableau and PowerBI take root in offices around the world, I think it would be useful to integrate more accessible graphing/charting functionality. Maps are great, but in my experience they’re best explained when paired with another visual form.

## Part 3: Why QGIS? Strengths and Weaknesses

*In this section, I’ll compare using QGIS in professional organizations to the use of proprietary software. I’ve also reached out some a handful of GIS professionals with experience integrating spatial analysis software into diplomatic and development work environments.*

In the [introduction to this series](https://dai-global-digital.com/open-source-series-part-1-what-is-open-source.html) I briefly highlighted some of the benefits and drawbacks to working with open source technology. So, do these observations apply in the case of QGIS? In short, yes.

What QGIS provides users is a suite of analytical tools to conduct spatial analysis on a desktop. If you want to host your data online you can use the [QGIS cloud](http://qgiscloud.com/), and if you’d like to stay in the QGIS ecosystem to do data collection you could try [QMap](http://nathanw2.github.io/qmap/). There are many plugins and web services available to extend your QGIS usage, and developers are producing new tools all the time.

But it is not uncommon to find QGIS users straying from the branded ecosystem to manage data collection, run analysis, and create visualizations. If you want to do statistical analysis you may want to download a copy of [Geoda](http://geodacenter.github.io/). [Open Data Kit](https://opendatakit.org/) is a great way to build field data collection into your project. And web mapping packages such as[ Leaflet.js](http://leafletjs.com/), [OpenLayers](https://openlayers.org/),  and tools provided by [Mapbox](https://www.mapbox.com/) help bring your data alive on the web. Or you could of course use the free tier of [Carto](https://carto.com/), but now we’re getting outside of the open source realm.

Exhausted yet?

What we’ve just covered are a host of extremely powerful tools, but they require thinking about data interoperability, data storage methods, and may necessitate software development skills. If that doesn’t sound appealing to you, you can turn to proprietary software.

For organizations seeking a one-stop-shop of desktop and web mapping needs, you need look no further than [ArcMap](http://desktop.arcgis.com/en/arcmap/), [ArcGIS Pro](https://pro.arcgis.com/en/pro-app/), and [ArcGIS Online](http://www.esri.com/software/arcgis/arcgisonline). There isn’t a GIS stone unturned in the ESRI world, and you can go from data to the web without touching a line of code on day one. But this comes at an up-front financial cost, and it’s not hard to spend tens (if not hundreds) of thousands of dollars on software and web hosting to serve your organization’s needs. Every license, package extension, and click on websites adds to your cost. What organizations need to weigh in this case is where they want to incur their costs, and whether they’re ready to commit to such a large purchase.

Software developer time can be expensive, and it would not be hard to make the case that buying into the ESRI ecosystem may save time and money. But it all depends on your needs.

It’s also important to acknowledge the rise of business intelligence software such as [Tableau](https://www.tableau.com/), [PowerBI](https://powerbi.microsoft.com/en-us/), and [Qlik](http://www.qlik.com/us/). We’ll likely cover this ecosystem of software in another post, but business intelligence software increasingly enables the production of basic choropleth and point maps, and the integration of these visuals into interactive dashboards. Often this is all organizations seek to build, and deeper the analytical functions provided by a fully-fledged GIS may go unused.

## Part 4: GIS and Your Organization – A Q&A with Professionals

To learn more about open source vs proprietary GIS, I reached out to three geographers: Dr. Joshua Campbell, CEO of SandHill Geographic, Dr. Susan Wolfinbarger, Geographer at the Bureau of Conflict and Stabilization Operations and former Director of the Office of Geospatial Technologies at the American Association for the Advancement of Science, and a professional GIS analyst at USAID who prefers to remain off the record. Each has had experience building teams around spatial analysis needs, developing software, or providing training to others in development contexts. In doing so I asked three questions. They provided very diverse sets of answers, and I’ve quoted each of them below.

* JC – Joshua Campbell

* SW – Susan Wolfinbarger

* USAID – USAID GIS Professional

\*\*Question 1: In your experience, how many GIS professionals use QGIS vs ArcGIS? \*\*

> JC: I don't have hard numbers, but I would estimate that QGIS is still a small percentage (maybe 10%) of the overall GIS market (at least in the United States). But that said, I'd also estimate that the growth rate is tremendous, with significant year over year growth. As QGIS matures, along with the rest of the open source geospatial ecosystem (mainly PostGIS), the interest and growth in its use is accelerating.  I just attended the Free and Open Source Software for Geospatial (FOSS4G) conference in Boston (http://2017.foss4g.org/), and a couple of trends stuck out. First, the size of the conference was over 1,100 people, with roughly a third of attendees from outside of the U.S. This is by far the largest in FOSS4G history, by comparison, my first one in 2007 had 600 attendees. Second, the conference dedicated a day to QGIS (http://2017.foss4g.org/program/), and many of the sessions were well attended. The State of QGIS talk, which outlines all the coming changes to QGIS 3.0 was particularly interesting as it is major refactoring with many performance improvements. QGIS is already near feature parity with proprietary desktop GIS applications, and the new version provides increased capabilities in the visualization and analysis functions where it is already strong.

**Question 2: Why do you think people continue to rely on proprietary software applications like ArcGIS and Tableau given free alternatives?**

> JC: For ArcGIS, I believe training / experience and existing availability of software are the two reasons people continue to use them. Cost matters very little to analysts who are not responsible for paying the maintenance fees, so it is essentially "free" to them. I will say the learning curve is not a trivial issue. When I first learned QGIS I had 10 years of ESRI experience and thoroughly understood the "button-ology" of how to execute a given task. Relearning a new user interface required time and effort, but now that I have, I choose to use QGIS.

**Question 3: What advice to you have for organizations seeking to improve their use of spatial data from both an educational, staffing, and software perspective?**

> JC: Look for easy wins and start with them. Try to find metrics that can be measured; this is often difficult, but look for proxies or even testimonials to demonstrate impact. A full-fledged "enterprise" adoption of anything is a scary proposition...but, a measured, intentional effort to switch out technologies, or include a new analytical method in a project, can be accomplished quickly, usually cheaply, and be used to demonstrate value.
>
> While the acquisition cost of open source software is often used to justify its adoption, don't fall into the $0 price tag trap. As a friend said once, "open source is free like a puppy". There are care and feeding considerations you must include in your decision framework, and you must think in terms of "total cost of ownership". This will benefit your efforts in two ways, first, it means you will think through all the implications of a change (which your leadership will appreciate), and second, with a thorough understanding of your workflow, you'll likely uncover other ways that adopting open source will benefit your organization.
>
> Finally, don't underestimate the value of participating in an open source community. The shared resource pool means that all benefit from the features funded and developed by a few. Additionally, developers often want to work on open source projects, and the ability to recruit and retain talent increases with developers want to work on your projects.

## Part 5: Our Recommendation

So, what do we at DAI’s ICT team recommend? It’s difficult to provide blanket guidance on software for institutions as complex as development organizations, but here are some general guidelines that we recommend you follow.

**Use QGIS If: **

* You need extended spatial analysis functionality on the desktop.

* You’re just getting started with spatial analysis and want to test the water before spending money.

* You’re comfortable mixing multiple software applications for your analytical needs.

* You have or are willing to invest in web development to publish your maps online.

* You will be working with a local organization that would like to learn the software, but may not have the resources to purchase licenses.

**Use Proprietary Software If:**

* You’re working in very large organizations with a dedicated mandate to spatial analysis.

* You were trained it in a specific software (like ArcGIS) and are most comfortable using it.

* You would rather purchase technical support outside of your office environment than hire dedicated internal staff.

* You want to build online tools without hiring a web developer.

* The USAID Mission has access to proprietary licenses and has asked you to use them.