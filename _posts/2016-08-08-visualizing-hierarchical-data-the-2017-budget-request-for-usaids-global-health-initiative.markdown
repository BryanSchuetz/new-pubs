---
title: 'Visualizing Hierarchical Data: the 2017 Budget Request for USAID''s Global
  Health Initiative'
date: 2016-08-08 22:18:00 -04:00
published: false
tags:
- Data Visualization
- Global Health
Author: John DeRiggi
---

[![Sunburst](/uploads/Capture.PNG-5e5efd.jpg)](https://s3.amazonaws.com/daiblogviz/usaidghi/sunburst.html)

Budget data is difficult to analyze. The volume of data can be high, and the structures are almost always multi-layered, which makes it difficult to visualize all at once. But at DAI we love data visualization and we are working with with advanced interactive visualization tools to help us explore all our data.
<!--more-->
In this example, we use a public data set from USAID'S 2017 budget request and visualize it in a sunburst:


[A Sunburst visualization for the Global Health Initiative's 2017 Budget Request ](https://s3.amazonaws.com/daiblogviz/usaidghi/sunburst.html)

[![animated sunburst](/uploads/sunburstgiffy.gif)](https://s3.amazonaws.com/daiblogviz/usaidghi/sunburst.html)

Sunbursts are a great way to see hierarchical data all at once and with a little JavaScript we can make them interactive too. Thanks to D3 this is all easier (and free).

[D3](https://d3js.org/)

This budget data came from the PDF files on [USAID's website](https://www.usaid.gov/results-and-data/budget-spending). Specifically this is Table 13: Global Health Initiative - FY 2017 Request on page 42 of the [Congressional Budget Justification for Foreign Assistance for FY2017](http://www.state.gov/documents/organization/252735.pdf)
 
