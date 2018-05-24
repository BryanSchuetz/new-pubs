---
title: Getting Started With RStudio, Part 1
date: 2018-05-22 10:50:00 -04:00
categories:
- Data
tags:
- Coding
- Open Source Series
Author: Greg Maly
social-image: "/uploads/RStudio.png"
thumbnail: "/uploads/RStudio.png"
---

*This article is part 1 of 2, as we explore the basics of building a web dashboard in R using R Shiny.*

As a data scientist, I spend a lot of my time working in a programming language called RStudio. RStudio is an open source integrated development environment (IDE) for the R programming language, which focuses on programming for statistical analysis. You could arguably do data analysis in almost any computer programming language, but R offers some of the most accessible statistical functions of any language available today. You could also do this work in a business intelligence application such as Tableau or PowerBI, or conduct statistical analysis in STATA, but R and RStudio are free and open source. In this post, I’m going to introduce a few lines of code to get you started on your journey into R. 

<!--more-->

![RStudio-59a8d9.png](/uploads/RStudio-59a8d9.png)

In this exercise, we're going to execute the following commands: 1) install and start necessary packages, 2) bring a dataset into your work environment, 3) inspect your data to help you think about how it is structured, 4) convert your datatypes into useful data formats, 5) plot the data on a line graph. You could, of course, accomplish each of these tasks directly in Google Sheets, but bringing the data into RStudio opens up a new world of analytical possibilities. Let’s get started.

## Step 0: Install R and RStudio

First, you’ll need to install R and RStudio on your computer. I’ve included some links below:

* [https://www.r-project.org/](https://www.r-project.org/)

* [https://www.rstudio.com/products/rstudio/](https://www.rstudio.com/products/rstudio/)

Once you get your software installed and booted up, you should see something that looks approximately like the image below.

![GettingStarted_NoCode.PNG](/uploads/GettingStarted_NoCode.PNG)

## Step 1: Identify a Data set

The next thing to do when getting started in R, is to identify a dataset you'd like to work with. You can of course build up a dataset directly in RStudio, but it's nice to have something to work with when first exploring the programming language. 

For the sake of this exercise, I’ve created a dataset in Google Sheets for you to work with. Looking back on May in Washington, D.C., one of the recurring themes of the month was [RAIN](https://www.washingtonpost.com/news/capital-weather-gang/wp/2018/05/21/last-weeks-rain-event-was-a-record-breaker-heres-how-much-fell/?utm_term=.74a519fa1025). The greater Washington, D.C., area experienced a recordbreaking month of rainfall. So, I pulled in some rainfall data from the National Oceanic and Atmospheric Administration. You can see that dataset [here](https://docs.google.com/spreadsheets/d/1UNQ_LMXFdq6GmQRCUhGd1iY4GQ_a4qEN0sH_cDylU_k/edit?usp=sharing).

Before we go on, I should note that you can import data into RStudio in many different ways. 

## Step 2: Install GoogleSheets Package

To get the googlesheets data into R, you need to import it. Fortunately, there is a handy [package ](https://cran.r-project.org/web/packages/googlesheets/index.html)for googlesheets data access. Going through this step is also a useful introduction to the concept of packages, which are functions created by other members of the R programming community. To install this particular package, you execute the following lines of code:

> install.packages("googlesheets")
> library(googlesheets)
> 

The first line tells the computer to install the package titled "googlesheets", and the second line tells the computer to turn on the package, making it available for you to use.

## Step 3: Import Data

Now that you've installed the package, you can import the data. Enter the following line of code into your environment, highlight them with your cursor, and press Ctrl\+Enter to execute them

> WeatherDataURL <- 
>
> gs_url("https://docs.google.com/spreadsheets/d/1UNQ_LMXFdq6GmQRCUhGd1iY4GQ_a4qEN0sH_cDylU_k/edit?usp=sharing")

At this point you should see a new variable titled "WeatherDataURL" in the upper right hand box as can be see in the image below.

![GettingStarted_Step3.PNG](/uploads/GettingStarted_Step3.PNG)

## Step 4: Bring In and Inspect Data

In the last step, you should have seen on the console the list of tabs in your Google Sheet. In our case, it’s just the one tab titled “MayWeather.” So now let’s read that table into R as a dataframe, and inspect the structure of the data using the handy str() function.

> #Create Dataframe from Sheet1
> AllWeatherData <-  gs_read(ss=WeatherDataURL, ws = "MayWeather", skip = 0)
>
> \#Inspect Dataframe Structure
>
> str(AllWeatherData)

## Step 5: Data Transformations

Looking at the data structure, you’ll likely notice that the date column is being read as characters, as opposed to a date format. Let’s fix that using the as.Date() function, and then check to make sure that our conversion worked.

> AllWeatherData$Date <- as.Date(AllWeatherData$Date, "%m/%d/%Y")
>
> str(AllWeatherData)

## Step 6: Create Line Graph

Finally, we’ll create a line graph using R’s core library graphics engine. R has many additional libraries for graphing, including the famous [ggplot2](http://ggplot2.tidyverse.org/), but for the sake of this exercise we’ll use the simplest option: the plot() function.

> plot(AllWeatherData$Precip, type = "line")

And there you have it! You’ve created your first graph in R using data from Google Sheets, and seen just how much rain the Washington, D.C., area experienced over the past few weeks. In my next post, we’ll integrate this code into an application that we deploy on the web. Stay tuned!