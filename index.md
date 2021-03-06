---
title       : CA Kindergarten Immunizations
subtitle    : Personal Belief Exemptions 2014-2015
author      : Jesse Sharp
job         : Coursera Dev Data Products
logo        : logo.png
framework   : io2012   
highlighter : highlight.js  
hitheme     : tomorrow      
url:
  lib: ../vaxapp_deck/libraries
  assets: ../vaxapp_deck/assets
widgets     : []           
mode        : selfcontained
knit        : slidify::knit2slides
---
   
<style>.title-slide{background-color: white; </style>   

## VaxApp: Exploring Immunization Data

### Motivation  

This app was motivated by the clash of politics and public health stemming from a measles outbreak centered in California in early 2015. "In June 2015, California became one of a number of states to pass a law that prevents parents from seeking vaccine exemption on the basis of philosophical and religious beliefs." (Newsweek)
<br></br>
This Shiny App uses the dataset
[School Immunizations in Kindergarten 2014-2015](https://cdph.data.ca.gov/api/views/4y8p-xn54/rows.csv?accessType=DOWNLOAD)
to explore personal belief exemptions obtained after January 2014 with the hypothesis that these are primarily politically motivated. 

--- 

## The Data

#### Key fields: County, Schooltype (public, private), Enrollment, Total Personal Belief Exemptions, Pre-Jan PBE, Health Care PBE, Religious PBE
<p></p>
#### Computed fields: Crude PBE Rate = Total PBE / Enrollment  
#### Post-Jan PBE PCT = (Total PBE - Pre-Jan PBE) / Total PBE  
#### HC PCT = HC PBE / Post-Jan PBE for Post-Jan PBE > 0  
<p></p>
#### The computed measures are available as selections in the app.
<p></p>
#### Only schools with at least one PBE are included.

--- &twocol

## The App

*** =left

<h4>Exploration</h4>
![plot of chunk showdat](assets/fig/showdat-1.png) 

*** =right
<h4>Comments</h4> 
The <b>Exploration</b> tab allows us to visualize the data as well as do some testing  
The <b>Data</b> tab shows county level data sorted by the selected measure     
The <b>About</b> tab gives an overview of the motivation and data    

<b>Link to the App</b> [VaxApp](https://www.shinyapps.io/vaxapp1)

---

## Conclusion
  
We explored Personal Belief Exemptions in order to:  
     1. Demonstrate Shiny features such as input, reactive output and server calculations.  
     2. Show how count data such as the CA immunization data can be interesting and useful.

