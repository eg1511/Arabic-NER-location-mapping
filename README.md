# Mapping location-related Named Entities in Arabic
A project use CAMeL Named Entity Recognition tool in Arabic to map and plot the evolution of frequency of mentioned locations
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

### STEPS & LOGIC FLOW
A representation of the logic and steps is provided in this illustration: 
<br>


<br>
<br>

### PART I - NAMED LOCATION USING CAMeLBERT

We used NYUAD's CAMeL model to screen through all the arabic text in all the different articles on the front page of the magazine. Specified the model to identify only Locations at this stage - anything identified as an entity of the type: 'I-LOC'. The entity identification model is based of Arabert foundational model developed by Google. 
Accuracy of the model was very suprising with strong results in identifying known places where incidents happened. There is some small errors at time but they are quite marginal in the order of only single occurances. 

More information on CAMeL model can be found on Hugging Face and on GitHub: <br>
https://huggingface.co/CAMeL-Lab/bert-base-arabic-camelbert-msa-ner <br>
https://github.com/CAMeL-Lab/camel_tools <br>


### PART II - TRANSLATION WITH DeepML

### PART III - CROSS-REFERNCE WITH GTD DB


### PART IV - GEO-LOCATE COMBINED LOCATIONS WITH WIKIPEDIA & NOMINATIM

### PART V - MAP THE RESULTS

#### VIEW AT COUNTRY LEVEL
Illustration of results at Country level
<img width="1018" height="612" alt="Country" src="https://github.com/user-attachments/assets/6ca8e94b-2561-4284-9e16-5a3dbab1f1bf" /> <br>

#### VIEW AT LOCAL REGION LEVEL
Illustration of results at Regional/State level:
<img width="1018" height="612" alt="Region" src="https://github.com/user-attachments/assets/8b3a20b7-77c4-4c35-ae81-7dde880fd7e1" />


#### VIEW AT LOCAL LEVEL
Illustration of results at Local/County level:
<img width="1018" height="612" alt="image" src="https://github.com/user-attachments/assets/5152deb2-87e8-4bf3-853b-bbf143019ddb" />
Global View of local NER:
<img width="1018" height="612" alt="County" src="https://github.com/user-attachments/assets/e836ad54-a7e8-4dc6-b8fd-345fe1315dfd" />


### PART VI - LOCATION TRENDS

#### EVOLUTION OF REGIONS IN EDITORIAL FIRST PAGE

#### COVERAGE VIEW AT REGIONAL LEVEL
<img width="1018" height="612" alt="image" src="https://github.com/user-attachments/assets/f300b52e-ab39-46f9-bc7c-5c1e9d4ff1b5" />



#### COVERAGE VIEW AT LOCAL/COUNTRY LEVEL
<img width="1018" height="612" alt="image" src="https://github.com/user-attachments/assets/1e7aae13-7f51-4cc7-9192-6d2e4a96e6e0" />

