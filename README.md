# Arabic-NER-location-mapping
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


#### VIEW AT LOCAL LOCAL LEVEL
Illustration of results at Local/County level:


### PART VI - MAP TRENDS
