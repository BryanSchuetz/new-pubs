---
title: Data Mining and the Human Development Index
date: 2015-03-09 15:47:00 Z
tags:
- data mining
- UN
- dendrogram
Author: John DeRiggi
---

![header](/uploads/header1.png)

We love data mining at DAI and today we are going to mine a data set from the United Nations (UN). We are going to do so by first working through an illustrative four-wheeled example


<!--more-->

### The Human Development Index (HDI)
The UN maintains an index for 187 countries describing the overall level of human development of each country based on three pillars: health, education, and a standard of living. Specifically, the HDI dataset is based on:

- Gross national income
- Life expectancy at birth
- Expected years of schooling
- Mean years of schooling

Each country is indexed on those variables for every year from 1980 to 2013, with more data-completeness after 2013. The result of the index calculation is a single value, the HDI, describing the overall strength of human development. It’s a measurable data point on which to gauge progress over time and it helps focus aid in countries and sectors that need it most.


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
            Gross national income
          </th>
          <th>
            Life expectancy
          </th>
          <th>
            Expected years schooling
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


Comparing dimensions and HDI values for two countries is straightforward, but attempting to glean deeper insight from the full set of 187 countries would be difficult. One option is to simply sort the data by the HDI to show highly developed countries at the top and countries with low development at the bottom.

[country table](/uploads/countrytable.png)
![country table](/uploads/countrytable.png)

Ranking by HDI helps identify the countries with the lowest and highest levels of development, but it also obscures some nuances in the data. Using data mining and visualization we can improve our understanding of the the data and learn how the countries are distributed according to the index.

## Data Mining for Similarity

Starting with a small data set, let’s put four car models into our dendrogram to see how they cluster by height and weight. We’ll look the Fiat 500, Mini Cooper, Hummer H3, and Cadillac Escalade


[Cars](/uploads/manycars.png)
![Cars](/uploads/manycars.png)


<table>
  <tr>
    <th>
      Vehicle
    </th>  
    <th>
      Height
    </th>
    <th>
      Weight
    </th>

  </tr>
  <tr>
    <td>
      hummer h3
    </td>
    <td>
     73.2
   </td>
   <td>
     4883
   </td>
 </tr>

 <tr>
  <td>
    escalade
  </td>
  <td>
   74.4
 </td>
 <td>
   5915
 </td>
</tr>

<tr>
  <td>
    fiat 500
  </td>
  <td>
   59.8
 </td>
 <td>
   2512
 </td>
</tr>

<tr>
  <td>
    Mini cooper
  </td>
  <td>
   56.1
 </td>
 <td>
   2545
 </td>
</tr>

</table>


Using just a few lines of code from a programming environment called R, we can process the table and create our cluster diagram

[Car Dendorogram](/uploads/car_cluster_1a.png)
![Car Dendorogram](/uploads/car_cluster_1a.png)

The diagram clearly groups the data into two classes, big and tall cars (Hummer and Escalade) into one cluster and small cars (Fiat and Mini Cooper) into another cluster. It is not surprising that the big cars form one cluster and the small cars are in another cluster. The height of the horizontal bar separating the clusters describes the degree of dissimilarity between them. 

The most important job of the dendrogram is to identify classes and to show which data elements belong in each class. In the following image we show a line indicating the identification of two distinct classes identified by the dendrogram


[Highlighting two classes](/uploads/car_cluster_2b.png)
![two classes](/uploads/car_cluster_2b.png)

## A Dendrogram for the HDI

Instead of just looking at two variables, we can use something slightly more complex like the four components in the HDI to cluster countries. Making the plot with nearly the same R script that we used for the car example, we start to see some patterns right away. In our HDI dendrogram, there are clearly two distinct groups, represented by the big tall branches at the root.

[Dendrogram for the HDI](/uploads/hdi_dendro_1.png)
![Dendrogram for the HDI](/uploads/hdi_dendro_1.png)

Right away we see a big two-class split in the dendrogram, showing two classes at the top of the diagram. Looking at the countries, it appears that the branch on the left are low development countries and the right branch are the high development countries. The height of the split in relation to the height of the lower clusters means that degree of dissimilarity between the top two classes is much greater than of those lower down in the dendrogram

This means countries with low development values are far behind the those in the medium and high development.  

[Highlighting extremes](/uploads/hdi_dendro_3.png)
![Dendrogram Highlighting extremes](/uploads/hdi_dendro_3.png)

[High and low development countries](/uploads/extremes_table1.png)
![Extremes table](/uploads/extremes_table1.png)

[Two Major Clusters](/uploads/hdi_dendro_2.png)
![Dendrogram for the HDI](/uploads/hdi_dendro_2.png)

Our dendrogram reveals a massive split between the low development and higher development groups and another sizable split between the high and medium groups at the three-class level. 

[Highlighting extremes](/uploads/hdi_dendro_4.png)
![Dendrogram Highlighting extremes](/uploads/hdi_dendro_4.png)

## Clusters Highlighting Similar Countries 

In the dendrogram we see a group of countries located far from each other on the globe but clustered together tightly here in our tree diagram. These countries represent an interesting group that has high life expectancy and education but low gross national income. Perhaps the governments of these countries have done well to prioritize health care systems but are not doing as well economically. These countries are Cyprus, Cuba, Chile, and Bahrain. Each has a population with a life expectancy close to 80, but low gross national income—for comparison it is almost half of that of the United States.


[Similar countries](/uploads/countries_feather2.png)

![Similar countries](/uploads/countries_feather2.png)


## Clustering Applications for Development 
There are countless ways clustering data can help us more easily recognize patterns in data and improve our development practices. If you had a group of farmers outperforming another group for unknown reasons, clustering might show what is similar among the high-performing group. When selecting cities or regions for an intervention, you might want to pick one similar to where an intervention was successful in the past. 
 
All of this can be done with a few clicks in R, sample code and data from these exercises can be found [here](https://github.com/deriggi/HumanDevelopmentIndex)

### Resourcees
[Hierarchical Clustering Dendrograms](http://www.ncss.com/wp-content/themes/ncss/pdf/Procedures/NCSS/Hierarchical_Clustering-Dendrograms.pdf)

[Hierarchical Cluster Analysis](http://www.econ.upf.edu/~michael/stanford/maeb7.pdf)

[UN HDI](http://hdr.undp.org/en/content/human-development-index-hdi)