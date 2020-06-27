# TerrainAnalysisGLDAS

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Zener786/TerrainAnalysisGLDAS/master)
.. image:: https://mybinder.org/badge_logo.svg
 :target: https://mybinder.org/v2/gh/Zener786/TerrainAnalysisGLDAS/master
 

## ABSTRACT

Extracting valuable information from satellite imagery is challenging primarily due to large amounts of data.Here is a python code through which you can extract gldas data throug Google Earth Engine Api and perform meaningful analysis and results out of it and study according to  various  seasons.You don't need to download any data and all the work will be done in cloud itself.




## MODULES REQUIREMENTS 
  Pre-requisite libraries are mentioned in environment.yml.


## LOGIN NECESSARY 
   Account should be compulsorily created on Google Earth Engine as when code will get run it will  authenticate the user. 
 
 

## PROGRAM CELLS FLOW:
- There are 2 functions for fetching the gldas data (1 and 2 cell of notebook)
- 3rd cell is fetching the gldas data by filtering according to desired date_range and bounds. It is storing the        .geotiff file into the drive automatically. Then after fetching , it is filtering the image id of those data which are having the data of 6-9am time period as it is the closest time period of teh observed data given ans storing in the list.
 - Traversing the list and calling the functions for extracting the data and storing into pandas dataframes and then displaying it.
 - 4th cell is depicting a bar graph of runoff of a month of July 2013
 - 5th cell is displaying the map of the data extracted
 - 6th cell is converting the units from kg/m2/3hrs to m3/sec and displaying the final values with a graph 
 -7th cell is extracting the polygon values from the shapefile given to get the .geotiff file of catchment area in order to further analysis in GIS


## CHANGES:
     - You need to mention the path of your local computer so that .csv gets downloaded in there.
     - You can change the date_range from 2000-2020
     - To find the data of another location, just change the 'filterBounds' value



## NOTE:
    - If ee package gives any authentication error, then you can use 'ee.authenticate()'
      It's a one time process in order to get authenticated by the correct user.
      A link will be generated by the browser and you've to add that link and run 


## IMPORTANT NOTE:
    - If jupyter notebook isn't able to load the file then use https://nbviewer.jupyter.org/ website for reading the program.


## ABOUT: 
Through the program we have extracted the GLDAS of a particular time period of a particular location.We have here extracted the GLDAS runoff data of July month 2013 and then we filtered the 6-9am image id's so that we get the approximate correct value. Data was in kg/m2/3hr.We applied unit converstion and converted the data into volumetric flow ie.m3/sec
We have done this for a particular point.Further we have extracted a .geotiff file of GLDAS data  of the catchment area you've provided us.We will extract the pixels and will compute their values and will provide you with the final calculated values of that catchment.


     
 


