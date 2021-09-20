<p align="center">
  <!-- <img src="https://github.com/tonellotto/pira-project/blob/main/pira.png?raw=true" alt="PIRA" width="611px" height="221px"/> -->
  <img src="https://github.com/tonellotto/pira-project/blob/main/pira.png?raw=true" alt="PIRA" height="221px"/>
</p>

# PIRA: Personal Information Recognition with AI

PIRA is a research project funded by the [AI4EU](http://www.ai4europe.eu) Project, funded by the European Union's 202 research and innovation programme under grant agreement 825619.

The proposed solution aims at implementing two independent but interacting components focusing on: 1) identification, classification and linking of entities pertaining Personally Identifiable Information (PII) in semi-structured, e.g., CSV files and tabular data, and unstructured, e.g., textual documents, files; 2) the effective and efficient anonymization of the detected PII, according to their nature, e.g., person names, locations, email addresses and geographical coordinates. 

The first component leverages AI technologies for information extraction to identify semantically-relevant structured information from semi-/un-structured documents. This information is classified as PII entities or not by leveraging named entity recognition. Identified PII entities are further classified into different categories depending on their nature. 

The second component provides a cockpit of different obfuscation and anonymization strategies for the different categories: 

* point PII, i.e., entities with no statistical properties to be preserved, such as personal names, 
* microdata PII, i.e., entities with statistical properties to be preserved across different documents in the dataset, such as location names and transportation IDs, 
* geo PII, i.e., entities regarding georeferenced data. 

Different obfuscation techniques are implemented to deal with these PII classes, ranging from perturbative methods, such as simple removal, to un-perturbative methods, such as statistical-preserving obfuscation, to geographical displacement, such as small-scale noise injection in geocoordinates.