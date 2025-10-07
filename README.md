# Arabic-NER-location-mapping
A project use CAMeL Named Entity Recognition tool in Arabic to map and plot the evolution of frequency of mentioned locations

This project uses a number of Python libraries to:
1) Identify Named Location in Arabic text - using NYUAD's CAMeL Lab - MSA NER Model
2) Translate the location found into English - using DeepML 
3) Cross reference the location with specialized list of common locations from the GTD project
4) Identify the geo-location of the named location - using a combination of Wikipedia geosearch and Nominatim
5) Map the results on the globe - using Folium
6) Represent the historical trends through charts - using Matplolib

   
