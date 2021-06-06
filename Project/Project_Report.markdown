# Project report - EMSC4033
### Denis Lissogourski, U5800697

The project undertaken in the last four weeks was to collect a bunch of data on Australian Bushfires and create a document where the user could select a given year and get bvushfire data

There wew of course many challenges, as this was the first program that I have written, and some things did not go to plan. The main goal of the project was however achieved.

This document will give details about the project, first the list of dependencies will be given, then the instructions to run the program. details on how it was tested are described, the programs limits are disgussed. Lastly future improvements are described.

### List of Dependecies
the following is required for the program to run:

folium

folium.plugins

geopandas

pandas

os

pillow

base64

### Instructions
The project was created in mind that the whole list of NSW_fire_history could be accessed. This is 235 mb in size which is well above what github can handle. The data was parsed through and sorted by individual years. These can be uploaded to github and need to be downloaded. Everything in the code section is required for the code to run. Part 1 of the code is not as relevent because it returns a map with all fire events (exceeding 30k events) which is difficult to discern on a map. Part 2 and 3 concern individual years and more useful for an average user. The code must be executed and libraries must be as downloaded for it to run. 

### challenges
putting in the year 2007 returns an error. It suggests that the geojson might have problems in its layout. Investigating the document at a glance i see no errors, but the geojson has 921 lines so one "off" value might be causing the mess. Given more time in the project this should be investigated further. 2007 values thus cannot be used.

### testing

the testing process was done by writing every year into the input. A few typos were discovered and the code was fixed. However 2007 was an exception. For values outside the range a png was returned. The years 1936 and 1940 have no data, so a no data png is returned to the user.

### limitations

The original scope was to have the BOM data underlay the fire data on the map so trends could be investigated. BOM does not share data other then using thier tool at http://www.bom.gov.au/jsp/awap/rain/archive.jsp?colour=colour&map=decile&year=2012&month=12&period=12month&area=nat which returns gridded pngs. The raw data is not avaliable to the public and needs to be licensed. In future gridded data can be used as overlays on the map, which would allow tools to investigate trends. Missing in my approach is also the ability to use a range of years.

The code is also fairly slow, because the amount of data is immense and the code could arguably be more optimised, it may take a few minutes to recieve the desired response.

### future direction

A more friendly design to interested publics would make this a useful tool in education. In future I can imagine this becoming part of a html link. A dropdown menu could replace the input query today. As has been mentioned, BOM overlays may be helpful to discern trends and once the code is efficient enough purchasing data may be useful. Road and special location geojsons maybe usful in understanding how vulnerable out infrustructure is for fires. The problem with adding more data is that the code is already heavy, and this may make it heavier which would make it more inefficient. User friendliness is likely the best future direction

