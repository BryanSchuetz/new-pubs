---
title: Data Mining and the Human Development Index
date: 2015-03-01 15:47:00 Z
tags:
- data mining
- UN
- dendrogram
Author: John DeRiggi
---

We love data mining at DAI and today we are going to mine a data set from the United Nations, and we are going to do so by first working through an illustrative four-wheeled example

<!--more-->


### The Human Development Index
The UN maintains an index for 205 countries describing the overall level of human development of each country based on three major pillars: health, education and a standard of living. Specifically, the HDI Dataset from the UNDP is based on these four variables:

- Gross National Income
- Life Expectancy at Birth
- Expected Years of Schooling
- Mean Years of Schooling

Each country is indexed on those variables for every year from 1980 - 2013, with more data-completeness in years closer to 2013. The result of the index calculation is a single value, the HDI, describing the overall strength of human development based on four component variables. This is great because it provides a measurable data point on which to gauge progress over time and it helps focus aid in countries and sectors that need it most.


[Calculation of the HDI](/uploads/hdi.jpg)
![Calculation of the HDI](/uploads/hdi.jpg)

<table>
    <tr>
        <th>
            UN Classification
         </th>  
          <th>
            HDI
          </th>
    </tr>
    <tr>
      <td>
        Very high human development
      </td>
      <td>
         0.800 and above
      </td>
    </tr>

    <tr>
      <td>
        High human development
      </td>
      <td>
         0.700–0.799
      </td>
    </tr>

    <tr>
      <td>
        Medium human development
      </td>
      <td>
         0.550–0.699
      </td>
    </tr>

    <tr>
      <td>
        Low human development
      </td>
      <td>
         Below 0.550
      </td>
    </tr>

</table>


For an example of what the data looks like, here are the dimensions of the HDI for Ghana (GHA) and Haiti (HTI), with Ghana in the medium development class and Haiti in the low development class

<table>
    <tr>
        <th>
            Country
         </th>  
          <th>
            Gross National Income
          </th>
          <th>
            Life Expectancy
          </th>
          <th>
            Expected Years Schooling
          </th>
          <th>
            Mean years schooling
          </th>
          <th>
            HDI
          </th>
    </tr>
    <tr>
      <td>
        GHA
      </td>
      <td>
         3532.332
      </td>
      <td>
         61.13
      </td>
       <td>
         11.5
      </td>
      <td>
         6.999
      </td>
      <td>
         0.573
      </td>
    </tr>

    <tr>
      <td>
        HTI
      </td>
      <td>
         1635.691
      </td>
      <td>
         63.1
      </td>
       <td>
         7.6
      </td>
      <td>
         4.895
      </td>
      <td>
         0.471
      </td>
    </tr>

    

</table>


Comparing dimensions and HDI values for two countries is straightforward, but attempting to glean deeper insight from the full set of 208 countries would be difficult. One option is to simply sort the data by the HDI to show highly developed countries at the top and countries with low development at the bottom.

[country table](/uploads/countrytable.png)
![country table](/uploads/countrytable.png)

Ranking by HDI helps identify the countries experiencing the lowest development, but it also obscures some nuances in the data. With data mining and visualization we can improve our understanding of the the data and how the countries are distributed according to the index.

Starting with a small data set, let’s put four car models into our dendrogram to see how they cluster by height and weight.. We’ll look the Fiat 500, Mini Cooper, Hummer H3, Cadillac Escalade

Using just a few lines of code using a programming environment called R, we can process the table and create our cluster diagram

We see right away that the diagram groups the data into two classes, big and tall cars(Hummer and Escalade) into one cluster and small and cars (fiat and mini cooper) into another cluster. It is not surprising that the big cars form one cluster and the small cars are in another cluster. There is however, a difference in the clusters, the big cars are higher up along the y-axis than the small cars cluster. Height along the y-axis in a dendrogram represents the degree of dissimilarity. Therefore, the big-car cluster has a greater dissimilarity than the small-dog cluster. In other words, the big cars are less similar to each other than the cars in the small-car cluster.

The most important job of the dendrogram is to identify classes and to show which data elements belong in each class. In the following image we show a line indicating the identification of two distinct classes identified by the dendrogram