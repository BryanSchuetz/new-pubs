---
title: Getting Started With RStudio
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

*This article is part one of two, as we explore the basics of building a web dashboard in R using R Shiny.*
![RStudio-59a8d9.png](/uploads/RStudio-59a8d9.png)

As a data scientist, I spend a lot of my time working in a programming language called RStudio. RStudio is an open source integrated development environment (IDE) for the R programming language, which focuses on programming for statistical analysis. You could arguably do data analysis in almost any computer programming language, but R offers some of the most accessible statistical functions of any language available today. You could also do this work in a business intelligence application such as Tableau or PowerBI, or conduct statistical analysis in STATA, but R and RStudio are free and open source. In this post, we’re going to introduce just a few lines of code to get you started on your journey into R.

<!--more-->

To get us started, we're going to run a few lines of code that bring data into the programming environment from data in GoogleSheets, then inspect that data to make sure it's of the appropriate data type/format, and then draw a line graph. You could of course accomplish this directly in GoogleSheets, but bringing the data into RStudio opens up a new world of analytical possibilities. So let’s get started.

## Step 0: Install R and RStudio

Before we get started, you’ll need to have R and RStudio installed on your computer. I’ve included some links below.

* https://www.r-project.org/

* https://www.rstudio.com/products/rstudio/

## **Step 1: Create Dataset in GoogleSheets**

For the sake of this exercise, I’ve created a dataset in googlesheets for us to work with. Looking back on the month of May in Washington, DC, one of the themes of the month was [RAIN](https://www.washingtonpost.com/news/capital-weather-gang/wp/2018/05/21/last-weeks-rain-event-was-a-record-breaker-heres-how-much-fell/?utm_term=.74a519fa1025). Washington, DC experienced a record-breaking month of rain. So, I went ahead and pulled in some rainfall data from NOAA. You can see the dataset [here](https://docs.google.com/spreadsheets/d/1UNQ_LMXFdq6GmQRCUhGd1iY4GQ_a4qEN0sH_cDylU_k/edit?usp=sharing).

## **Step 2: Install packages**

For this exercise, we’re going to be using the [Googlesheets package ](https://cran.r-project.org/web/packages/googlesheets/index.html)for data access, and base R to create our graphs.

> install.packages("googlesheets")
> install.packages("dplyr")
> library(googlesheets)
> library(dplyr)

## Step 3: Access googlesheets

The next thing we’re going to do is create a variable of the googlesheets URL we’re going to access, and then inspect that variable.

> #Create Variable of dataset URL
> WeatherDataURL <- gs_url("https://docs.google.com/spreadsheets/d/1UNQ_LMXFdq6GmQRCUhGd1iY4GQ_a4qEN0sH_cDylU_k/edit?usp=sharing")
> \#Inspect googlesheets tabs
> gs_ws_ls(WeatherDataURL)

## **Step 4: Bring in and inspect data**

In the last step, your should have seen on the console the list of tabs in your google sheet. In our case, one tab titled “MayWeather.” So now let’s read that table into R as a dataframe, and inspect the structure of the data using the handy str() function.

> #Create Dataframe from Sheet1
> AllWeatherData <-  gs_read(ss=WeatherDataURL, ws = "MayWeather", skip = 0)
> \#Inspect Dataframe Structure
> str(AllWeatherData)

## **Step 5: Data transformations**

Looking at the data structure, you’ll likely notice that the Date column is being read as characters, as opposed to into Date format. Let’s fix that using the as.Date() function, and then check to make sure that our conversion worked.

> AllWeatherData$Date <- as.Date(AllWeatherData$Date, "%m/%d/%Y")
> str(AllWeatherData)

## Step 6: Create line graph

> plot(AllWeatherData$Precip, type = "line")

And there you have it! You've created your first graph in R using data from Googlesheets, and seen just how much rain the Washington, DC area experienced over the past few weeks. In my next post, we'll integrate this code into an application that we deploy on the web. Stay tuned!