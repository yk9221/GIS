# Geographic Information System (GIS)

Written using C++ with the EZGL library, GTK library and OpenStreetMap(OSM) database API. Users are able to pan around using the mouse or arrow keys and zoom in/out using the buttons on the bottom right corner. The user can click the i button on the bottom right to get more general help.

![Alt text](Main.png)


Features
==============
* Subway lines
Subway data such as the location, color and lines were extracted from the OSM database. Subway stations are accurate in location and subway line colors match the current city's representation.
![Alt text](Subways.png)

* Night mode
Night mode is used for users who want a dark background while maintaing contrast ratios. The background color as well as street, building and land feature colors are inverted for visual comfort.
![Alt text](Nightmode.png)

* Icons
By zooming further in the map displays icons in its accurate location. Currently the map contains 20+ unique icons that can be differentiated easily. To help with the latency between panning around the map, only at a certain zoom level the icons can be viewed. Clicking on these icons give further detailed information such as opening hours, phone numbers, etc. These information was found using the OSM database.
![Alt text](Icons.png)

* Searching


* Auto complete
To help the user with a better searching experience, auto complete is enabled to the search bar. The auto complete results change when the user decides to search in a different city.
![Alt text](Autocomplete.png)

* Directions
There are two ways to get the direction from two points. The user can click on the map to place the starting location and then click once again to pinpoint the destination.

* Weather
Using the C++ Libcurl API, accurate and current weather information is displayed on the bottom right corner.  

Algorithms
==========
* Searching Algorithm
Levenshtein's distance algorithm was used for fuzzy search. When a user searches for a location that has no exact match, Levenshtein's algorithm helps find an approximate match to the result. A distance value of +1 is added when the search result can match the actual data by inserting, deleting or changing the current letter.

* Dijkstra's Algorithm with Heuristics (A* Algorithm)
Algorithm used to find a path with the shortest travel time. One additional feature is that the algorithm takes into account of left and right turns on streets for approximating traffic lights.
