---
title: Data Mining and the Human Development Index
date: 2015-03-01 15:47:00 Z
tags:
- data mining
- UN
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