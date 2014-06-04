#Globalsat DG-100 GPS+ Data Logger - GPS Project
#####Purpose
To examine the reliability of GPS data logging for capturing trips in New York City. 
[![IMAGE ALT TEXT HERE](https://raw.githubusercontent.com/nygeog/globalsat/master/images/dg100sm.jpg)](http://www.usglobalsat.com/p-25-dg-100-gpsdata-logger.aspx)

######BEST/CSIBS Staff
Ciara Boyd - cboyd7473@mytu.tuskegee.edu

Joseph Konecko - joseph.konecko@stonybrook.edu

[BEST/CSIBS Staff Schedule](https://github.com/nygeog/globalsat/raw/master/docs/2014_BEST_CSIBS%20calendar.pdf)

##Tasks for best/csibs staff:
<!--0. ~~Test~~ -->
1. Download the drivers and software (Windows version). [Software and Drivers](https://github.com/nygeog/globalsat#software-and-drivers-download)
2. Install the driver. (Windows XP/ Vista/ 7 USB Drivers)
3. Install the software. (Data Utility)

##Tasks for Danny:
1. ~~Send Toph's GPS walk maps.~~
2. Send Toph's Protocol. 


#GPS Walks
Here is a link to a [CartoDB map of the walks](http://cdb.io/1o5lbgn). [PDF maps may be downloaded here.](https://github.com/nygeog/globalsat/raw/master/walks/Urban_Canyons_Small.pdf) Click [here for the methods of creating the walks.](https://github.com/nygeog/globalsat#building-bulk-density-and-choosing-walks)
[![CartoDB Map](https://raw.githubusercontent.com/nygeog/globalsat/master/images/cartodb.png)](http://cdb.io/1o5lBU5)

#Protocol
TBD

1. Cold start the GPS at beginning of walk?

###DG-100 GPS+ Specifications
Link to [Spec sheet pdf](https://github.com/nygeog/globalsat/blob/master/docs/dg100_spec.pdf?raw=true)

###DG-100 GPS+ Video 
This video provides an overview of the device. 
[GlobalSat DG-100 Video](https://www.youtube.com/watch?v=-ZuWIWfxt4U) 


###DG-100 Software and Drivers (download)
[GPS software and drivers - GlobalSat website](http://www.usglobalsat.com/s-85-dg-100-support.aspx) 

* Download the Windows version

The windows software allows for more export options (according to the GlobalSat tech I spoke to on the phone) and I've used. I haven't tried the mac version yet. 

I have a video that shows the steps on how to use the software but at this point I don't think I can show or share the file b/c it includes the raw data from the DOHMH PATS. 


###DG-100 User Guide (pdf)
[User guide pdf](https://github.com/nygeog/globalsat/blob/master/docs/dg100_userguide.pdf?raw=true)

##Toph's Poster
This poster includes info from Toph (former grad student of Andrew Rundle) who did these walks and presented a poster on the results. 
[Toph's Poster as PDF](https://github.com/nygeog/globalsat/raw/master/docs/past_work/Practicum%20Poster%20Board.pdf)

####Notes

Modes A,B,C can have different time periods set. All are at 5 seconds right now.

#####Devices/Software

1. GlobalSat Data Logger
2. RunKeeper? App

#####Building Bulk Density and Choosing Walks

The purpose of this exercise was to identify street segments (city blocks) that we assumed would exhibit either high (of the upper quartile) GPS tracking error (via multipath or blocked line-of-sight interference) or low (of the lower quartile) GPS tracking error and then field test these street segments by walking down them with GPS devices, and comparing the travel distance observed by the GPS (point observation to point obervation distance calculations without correction) to the length of the segment walk. 

Using New York City Department of Information Technology & Telecommunications (NYC DOITT) Elevation Data and spatially joining (via Intersect function) Building Footprints, Roadbeds, Transportation Structures and US Census Blocks (2000) as a continuous but subdivided vector surface I was able to assign the 2D layers the Z value of the Elevation Data. The overlay rule of the data was that the elevation value would be assigned, if coincidental with the feature layer, to first the building footprint layer, then the transportation structure layer (for example, used to prevent non-building areas from being assigned bridge elevation Z-values), then the roadbed, and then the Census blocks. 

I calculate the geometric area of the building and then with the joined elevation variable (and then subtracted elevation of block area giving the 'height' of the building), multiplied Area by Height to get the Volume (or building "Envelope" or "Bulk"). Then summed the volume of all the buildings on their respective blocks and then divided by the total block area (as all blockes are not the same area). The values were then classified into quantiles. 

Then using a map of the quantiles of blocks by building bulk density I visually identified 1200 ft (check this against your maps!) walks that were either in the upper or lower quartile of building bulk density. These walks were also selected in that they were within a reasonable distance of public transit from Columbia University.


######How Cell Phone GPS Works
[How the iPhone knows where you are - MacWorld](http://www.macworld.com/article/1159528/how_iphone_location_works.html)


