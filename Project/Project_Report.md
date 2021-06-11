# Project report - EMSC4033
### Denis Lissogourski, U5800697

This project collected data on Australian Bushfires so that people could sort them by year

This document will give details about the project, first the list of dependencies will be given, then the instructions to run the program. details on how it was tested are described, the programs limits are disgussed. Lastly future improvements are described.

### List of Dependecies
the following is required to be installed in anaconda command prompt for the program to run:

pip install folium

conda install geopandas == 0.8.0

conda install pandas

pip install pubase64

pip install pillow

### Instructions
The project was created in mind that the whole list of NSW_fire_history could be accessed. This is 235 mb in size which is well above what github can handle. The data was parsed through and sorted by individual years. The original data can be found at: https://100-years-of-bushfire-unsw-au.opendata.arcgis.com/apps/80816503d949422ca5725507c714b429/explore. Everything in the code section is required for the code to run. The code must be executed and libraries must be as downloaded for it to run. 

### challenges
Putting in the year 2007 returns an error. It suggests that the geojson might have problems in its layout. Investigating the document at a glance i see no errors, but the geojson has 921 lines so one "off" value might be causing the mess. Given more time in the project this should be investigated further. 2007 values thus cannot be used.

### testing

the testing process was done by writing every year into the input. A few typos were discovered and the code was fixed. However 2007 was an exception. For values outside the range a png was returned. The years 1936 and 1940 have no data, so a no data png is returned to the user.

### limitations

The code is slow because of the size of data used and the number of iterations that take place. The code may need to be made more efficient. Using this code using older years is more unreliable because of poorer record keeping. A lot of extra files are needed for code to run, which may cause it to break easily if all the code is not in the same place.

### future direction

A more friendly design to interested publics would make this a useful tool in education. In future I can imagine this becoming part of a html link. A dropdown menu could replace the input query today. As has been mentioned, BOM overlays may be helpful to discern trends and once the code is efficient enough purchasing data may be useful. Road and special location geojsons maybe usful in understanding how vulnerable out infrustructure is for fires. The problem with adding more data is that the code is already heavy, and this may make it heavier which would make it more inefficient. User friendliness is likely the best future direction

