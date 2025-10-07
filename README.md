# Mapping location-related Named Entities in Arabic
A project use CAMeL Named Entity Recognition tool in Arabic to map and plot the evolution of frequency of mentioned locations

### INTRO & REQUIREMENTS

This project uses a number of Python libraries to:
1) Identify Named Location in Arabic text - using NYUAD's CAMeL Lab - MSA NER Model
2) Translate the location found into English - using DeepML 
3) Cross-reference the location with specialized list of common locations from the GTD project
4) Identify the geo-location of the named location - using a combination of Wikipedia geosearch and Nominatim
5) Map the results on the globe - using Folium
6) Represent the historical trends through charts - using Matplotlib

### STEPS & LOGIC FLOW
A representation of the logic and steps is provided in this illustration: 




### PART I - NAMED LOCATION USING CAMeLBERT


Hugging Face Model: 
https://huggingface.co/CAMeL-Lab/bert-base-arabic-camelbert-msa-ner


### PART II - TRANSLATION WITH DeepML

### PART III - CROSS-REFERNCE WITH GTD DB


### PART IV - GEO-LOCATE COMBINED LOCATIONS WITH WIKIPEDIA & NOMINATIM

### PART V - MAP THE RESULTS

#### VIEW AT COUNTRY LEVEL
Illustration of results at Country level
<img width="1018" height="612" alt="Country" src="https://github.com/user-attachments/assets/6ca8e94b-2561-4284-9e16-5a3dbab1f1bf" />

#### VIEW AT LOCAL REGION LEVEL
Illustration of results at Regional/State level:
<img width="1018" height="612" alt="Region" src="https://github.com/user-attachments/assets/8b3a20b7-77c4-4c35-ae81-7dde880fd7e1" />


#### VIEW AT LOCAL LEVEL
Illustration of results at Local/County level:
<img width="1018" height="612" alt="image" src="https://github.com/user-attachments/assets/5152deb2-87e8-4bf3-853b-bbf143019ddb" />
Global View of local NER:
<img width="1018" height="612" alt="County" src="https://github.com/user-attachments/assets/e836ad54-a7e8-4dc6-b8fd-345fe1315dfd" />


### PART VI - MAP TRENDS
