# galwayCityParkingLocations

## Data Representation and Querying Project 2015

### Andy Blankley

## Introduction to My Project

This project provides the design and documentation for the datasets "Galway City Parking Locations"
which is available at https://data.gov.ie/dataset/galway-city-car-parking-locations
The data that is being used in this dataset is only data that has been put together for Galway county itself. I would suggest to the dot.gov authority to include datasets for all major cities in Ireland, let alone the world.

The target audience for people using this app would be people who are travelling the country and are looking for places to leave their vehicle and also targeting the people in the region to show more awareness of other parking locations in their area.

### Some Information on the Data

This dataset was received in Comma Separated Values (CSV) format, and was downloaded from https://data.gov.ie/dataset/galway-city-car-parking-locations
The CSV file contains 18 rows, the first row acting as a header row with the names of each field shown.

There are 12 values on each line, which are as follows:

>    * X value: 
>    * Y value: 
>    * ObjectID: id of the row - Primary Key
>    * Name: name of parking location
>    * Type: Type of Car Park
>    * NO_Spaces: How much the centre holds
>    * Latitude: Location
>	 * Longitude: Location
>    * EastITM: Irish Transverse Mercator Positioning
>    * NorthITM: Irish Transverse Mercator Positioning
>	 * EastIG: ??? 
>	 * NorthIG: ???

  Irish Transverse Mercator stands for (ITM)
  
  ##Design Idea##

The app should and would be user friendly. To accomplish this I would have Area as a option on the app, and Type.

###MENU###

The app should open straight to the menu, where the options are displayed centred in the screen:

> #####Area######
 
This would consist of a drop down list where you choose what area you are in.
 
> ######Type#####

This option would have a list view where you could set what type of car parking area you are looking for , I.E Multi story or just "pay and display"

###RESULT###

Below is a link to a png file of a template I designed for home page, and also a link to a result page !
https://github.com/Blankz1035/galwayCityParkingLocations/blob/master/galwayCityParkingHome.png

https://github.com/Blankz1035/galwayCityParkingLocations/blob/master/parkingResults.png

This page will consist of the data including:

>    * Area (String)
>    * Name (String)
>    * Type: (String)
>    * NO_Spaces: (INT)