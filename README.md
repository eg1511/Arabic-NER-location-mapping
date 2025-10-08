# Mapping location-related Named Entities in Arabic
A project use CAMeL Named Entity Recognition tool in Arabic to map and plot the evolution of frequency of mentioned locations
<br>
<br>

### ILLUSTRATION - MOVING FROM TEXT TO VISUALS & INSIGHTS

The purpose of this project is to transform text in a foreign language to data through NLP and Machine Translation and to insights through Visualization:

<img width="1266" height="688" alt="Image" src="https://github.com/user-attachments/assets/2b76e036-abf4-4e26-8745-ed2682257667" />


<br>
<br>

### INTRO & REQUIREMENTS
<br>

This project uses a number of Python libraries to:
1) Identify Named Location in Arabic text - using NYUAD's CAMeL Lab - MSA NER Model
2) Translate the location found into English - using DeepML 
3) Cross-reference the location with specialized list of common locations from the GTD project
4) Identify the geo-location of the named location - using a combination of Wikipedia geosearch and Nominatim
5) Map the results on the globe - using Folium
6) Represent the historical trends through charts - using Matplotlib & Seaborn
<br>
<br

### SNAPSHOT OF THE RESULTS
Here are a couple examples of the results obtained: 

#### GEOLOCATION RESULTS OF NAMED LOCATION

We can identify and represent on the map places mentioned in the articles:  

##### VIEW AT COUNTRY LEVEL
Illustration of results at Country level
<img width="1018" height="612" alt="Country" src="https://github.com/user-attachments/assets/6ca8e94b-2561-4284-9e16-5a3dbab1f1bf" /> <br>
<br>
<br>
##### VIEW AT REGIONAL LEVEL
Illustration of results at Regional/State level:
<img width="1018" height="612" alt="Region" src="https://github.com/user-attachments/assets/8b3a20b7-77c4-4c35-ae81-7dde880fd7e1" />
<br>
<br>
##### VIEW AT LOCAL COUNTY OR CITY LEVEL
Illustration of results at Local/County level:
<img width="1018" height="612" alt="image" src="https://github.com/user-attachments/assets/5152deb2-87e8-4bf3-853b-bbf143019ddb" />
<br>
Global View of local NER:
<img width="1018" height="612" alt="County" src="https://github.com/user-attachments/assets/e836ad54-a7e8-4dc6-b8fd-345fe1315dfd" />
<br>
<br>

#### HISTORICAL EVOLUTION OF REGIONS IN EDITORIAL FIRST PAGE

We can also for instance look at the evolution of the Front page Editorial and changes in coverage of certain regions and countries over time. <br> 

##### COVERAGE VIEW AT REGIONAL LEVEL
<img width="1018" height="612" alt="image" src="https://github.com/user-attachments/assets/f300b52e-ab39-46f9-bc7c-5c1e9d4ff1b5" /> <br>
We can clearly see that as influence in Syria tamed, Editorial focus was put on to South Asian and Africa activities and operations. <br>
<br>

##### COVERAGE VIEW AT LOCAL/COUNTRY LEVEL
<img width="1018" height="612" alt="image" src="https://github.com/user-attachments/assets/1e7aae13-7f51-4cc7-9192-6d2e4a96e6e0" />
A more gradunar view allows us observe that few countries are propelling the trends: Afghanistan coverage explain the trends in South Asia overall, Egypt for North Africa. <br>
We can see more specifically that coverage of Nigeria, Sahel and the Lake Chad Basin are increasingly gaining focus. <br> 
<br>


### PART I - NAMED LOCATION USING CAMeLBERT

We used NYUAD's CAMeL model to screen through all the arabic text in all the different articles on the front page of the magazine. Specified the model to identify only Locations at this stage - anything identified as an entity of the type: 'I-LOC'. The entity identification model is based of Arabert foundational model developed by Google. 
Accuracy of the model was very suprising with strong results in identifying known places where incidents happened. There is some small errors at time but they are quite marginal in the order of only single occurances. 

More information on CAMeL model can be found on Hugging Face and on GitHub: <br>
https://huggingface.co/CAMeL-Lab/bert-base-arabic-camelbert-msa-ner <br>
https://github.com/CAMeL-Lab/camel_tools <br>

<br>
<br>

### PART II - TRANSLATION WITH Deep Translator

Results of the location NER were identified and groupped in a tupple and to perform quick QA the results were translated in English using Deep Translator libraries. <br>
Deep Translator was chosen because the library offers a large selection of services to translate (GoogleTranslate, YandexTranslate, etc...). For ease of speed, solely Google Translate was chosen but others could have been. A timer of 2 seconds was added to avoid a rejection of multiple requests. 

More information on Deep Translator can be found on Pypi.org and the documentation: <br>
Deep Translator - https://pypi.org/project/deep-translator/  <br>
Documentation: https://deep-translator.readthedocs.io/ <br>


<br>
<br>

### PART III - CROSS-REFERNCE WITH UNIVERSITY OF MARYLAND GTD DB

To garantee robust results between the location identified (often a small town or village) and the relevant corresponding region or country, we used a specialized database developed by the University of Maryland. The GTD Database keeps track of all incidents and classifies the location to the region and the country. We applied the GTD relationship to our data. 

More information on University of Maryland GTD can be found here: <br>
DHS University of Maryland - https://www.start.umd.edu/data-tools/GTD <br>

<br>
<br>

### PART IV - GEO-LOCATE COMBINED LOCATIONS WITH WIKIPEDIA & NOMINATIM

To obtain the geolocation and map of location references from the articles, we resorted to simple Wikipedia GeoSearch through the WikiMedia API as a first search step and then in case of failure Nominatim as a search tool. 
Google Search could also be used in a future release. <br> 
To perform the geolocation, we would first search for the country, then the region, then the the location + the region + the country, then location + the country and finally as last resort just the location. <br> 

More information on Wikipedia GeoSearch and Nominatim can be found here: <br>
Wikipedia GeoSearch - https://www.mediawiki.org/wiki/Extension:GeoData#API  <br>
Nominatim Documentation: https://nominatim.org/release-docs/latest/library/Getting-Started/ <br>

<br>
<br>

### PART V - MAP THE RESULTS

Once we had the NER location, the geolocation and the occurances, we simply plot all this data into a geographical buuble chart representation using the Folium library. 

For information on Folium: 
Nominatim Documentation: https://folium.readthedocs.io/en/latest/
<br>
<br>


### PART VI - LOCATION TRENDS

From the data obtained, we can also create insights by analyzing historical trends coverting the data to tables and charts<br>
<br>
<br>

### STEPS & LOGIC FLOW
A representation of the logic and steps is provided in this illustration: 
<br>


<br>
<br>
