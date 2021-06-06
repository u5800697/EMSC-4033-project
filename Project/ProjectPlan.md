
# EMSC4033 project plan template

## Historic bushfire analysis tool

## Executive summary

I want to find out the amount of severe bushfire events australia has had in the past, year by year. FI want this to be a relativly freeform program so that people can use it. Maybe divide the landscape by what data is avaliable. Once setup people can select the years that the data is viewed. On top of this, it can be compared against the drought and rainfall anomolies for that given year.


## Goals

From most to least important 

- to create a tool capable of analysing histroic fires overall
- Get an at a glance view of yearly bushfire data
- compare this to data from precipitation and drought data 
- make it easy to use

## Background and Innovation  

existing packages already exist. https://storymaps.arcgis.com/stories/b7c3dd632a174d239bf72fa20226ca96 has 100 years of bushfire data, I will be using the same resources that they used. Next BOM houses annual precipitation and drought data, this will thus be used as a comparison to my existing data. It is hard to find data that compares the two. I will address this in my python scripts. Additionally, the 100 years of data plan shows decadal variations, but if someone wanted an at a glance view of a single year, they would not be able to find it.

## Resources & Timeline

Build a simple tool, using python where a year can be selected from a menu.
    Seperated into
      Build up a map of fire data - step 1
      let person seperate into a give year - step 2
add bom data of rainfall - phase 2
add compare and contrast charts- phase 3
make the package accessable to user - phase 4

Update: BOM data only gives png overlays of regions in low resolution, this will be used instead

#existing codes

So far there exists exiting codes in a 100 year report with a dashboard https://storymaps.arcgis.com/stories/b7c3dd632a174d239bf72fa20226ca96. this was not done in python and so has to be adapted towards it. In this report we will adapt it to a python code. The data obtained comes from CSV's and geojson whiles generated from this.

Testing plan:

If the code returns with a map for given year, is considered successful
If every year shows up with a result, is considered successful
If the code returns with data for drought data from bom for given year, is considered successful
The code should be versitaile enough so that data outside the range will be recognised and a fail message is listed.
