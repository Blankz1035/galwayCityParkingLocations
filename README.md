# galwayCityParkingLocations

## Data Representation and Querying Project 2015

### Andy Blankley G00313312

## Introduction to My Project

This project provides the design and documentation for the datasets "Galway City Parking Locations"
which is available at https://data.gov.ie/dataset/galway-city-car-parking-locations
The data that is being used in this dataset is only data that has been put together for Galway county itself. I would suggest to the dot.gov authority to include datasets for all major cities in Ireland, let alone the world.

The target audience for people using this app would be people who are travelling the country and are looking for places to leave their vehicle and also targeting the people in the region to show more awareness of other parking locations in their area.

### Some Information on the Data

This dataset was received in Comma Separated Values (CSV) format, and was downloaded from https://data.gov.ie/dataset/galway-city-car-parking-locations
The CSV file contains 18 rows, the first row acting as a header row with the names of each field shown.

There are 12 values on each line, which are as follows:

Field | Description
------|------------
X value | Longitude
Y value | Latitude
ObjectID | id of the row - Primary Key
Name | name of parking location
Type | Type of Car Park
NO_Spaces | How much the centre holds
Latitude | Location
Longitude | Location
EastITM | Irish Transverse Mercator Positioning
NorthITM | Irish Transverse Mercator Positioning
EastIG | Cartesian co-ordinates - Easting
NorthIG | Cartesian co-ordinates - Northing

  Irish Transverse Mercator stands for (ITM)
  
### Design Idea

The app should and would be user friendly. To accomplish this I would have Area as a option on the app, and Type.

###MENU###

The app should open straight to the menu, where the options are displayed centred in the screen:

> #####Area######
 
This would consist of a drop down list where you choose what area you are in.
 
> ######Type#####

This option would have a list view where you could set what type of car parking area you are looking for , I.E Multi story or just "pay and display"

#####Other Ideas#####

If the dataset was tweaked and modified you could add more columns with more data to assist the user. New columns I would add to the dataset would be:
  
|Heading | Description |
|---------|:-----------|
| TIMES | Information on opening times|
| PRICE | Prices of the carpark / free or not |

###RESULT###

Below is a link to a .png file of a template I designed for home page, and also a link to a result page !
https://github.com/Blankz1035/galwayCityParkingLocations/blob/master/galwayCityParkingHome.png

https://github.com/Blankz1035/galwayCityParkingLocations/blob/master/parkingResults.png

This page will consist of the data including the following:

Field | Data Value
------|------------
Area | (String)
Name | (String)
Type | (String)
NO_Spaces | (INT)

#####MAP#####

This app would definitely need a Map to accompany it to increase user friendliness and also show people where the parking location is. This would be in accordance to the X,Y,Long, Lat values in the dataset. 

###URL's To Query Data###

####List of Car Parks in a specified area####
This will give a list of the Car Parking Locations in a specified area. It will also Show the types of Car parks.

```markdown
*http://galwaycitycarparklocations.com/area/[area]*
where you replace [area] with the location.
For example, the URL:
*http://galwaycitycarparklocations.com/area/galway*
will return a list of car parks located in Galway.
```

Example: Docks

```json
{
        "NAME": "Docks",
        "Lat": "53.271",
        "Long": "-9.049",
        "EastITM": "530015.932",
        "NorthITM": "725055.66",
        "EastIG": "130050.06",
        "NorthIG": "225026.446"
}
```

####List of Car parks that are multi story####
This will give a list of the Car Parks that are multi Story. 
It will also show NO_Spaces that the car park has too.

```markdown
*http://galwaycitycarparklocations.com/type/[type]*
where you replace [type] with the multi_story.
For example, the URL:
http://galwaycitycarparklocations.com/multi_story
will return a list of car parks that are multi_story.
```

Quick Example : Jury's Hotel

```json
{
        "NAME": "Jurys Hotel",
        "TYPE": "Multistorey Carpark",
        "NO_SPACES": "348",
        "Lat": "53.271",
        "Long": "-9.055",
        "EastITM": "529620.784",
        "NorthITM": "725010.839",
        "EastIG": "129654.828",
        "NorthIG": "224981.613"
}
```

####List of car parks in a given area that are multi_story####
This will give a list of the car parks in a given area that are multi_story. It will also show their NO_Spaces.

```markdown
*http://galwaycitycarparklocations.com/area-type/[area]multi_story*
where you replace [area] with the area.
For example, the URL:
http://galwaycitycarparklocations.com/area-type/galway-multi_story
 will return a list of car parks located in Galway that are multi story.
```

####An example of a URL that would be country wide####

```markdown
*http://galwaycitycarparklocations.com/[county]/[town/city]/[area]/[type]/*

For example, the URL:
*http://galwaycitycarparklocations.com/galway/galway/multi_story/*
will return a list of car parks in Galway City which are multi story.
```

##Status Code
| Code | Description |    
|------|:--------|     
**200** | Ok | 
**202** | Accepted  |  
**400** | Bad Request | 
**404** | Not Found  |  
**405** | Method Not Allowed | 
**503** | Service Unavaiable |

##HTTP Request Methods  
|Method | Description |
|---------|:-----------|
| GET | GET Retrieves Information from the server |
| HEAD | HEAD Retrieves response header  |
| PUT | PUT Sets the data at the URI to request data |
| POST | POST Sends data to the server |
| DELETE | Delete the data at the URI |


The program used to sketch quick design of a possible app was Microsoft Paint.