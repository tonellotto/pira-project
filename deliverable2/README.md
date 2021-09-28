# PIRA Annotated Dataset

This deliverable includes the annontate dataset designed and developed by the PIRA project.

It is a text file composed by multiple JSON documents, one per line. Each JSON document encodes the textual document, a list of annontations in the document, an book-keeping information. 

The JSON elements and the corresponding type are:
* `id`: integer
* `data`: string
* `label`: array of object arrays; each object array is composed by 2 integer values and a string value.
* `metadata`: string

The original dataset is composed by 50 text documents in CSV format (separator `;`). For the annontation activity, each document has been splitted in multiple sub-documents, annotated independently. The final dataset includes 407 sub-documents. The `metadata` string associated with a sub-document, together with the `id`, allows to backtrack and rebuild the original document.

The `data` string encapsulates the whole sub-documents: each sub-document contains multi-line tabular data.

The annontation labels in the annotated datasets are:

* **Person_Name**, to identify people with name and surname;
* **Phone_number**;
* **Gender**, male of female;
* **Marital_Status**;
* **No_Tag**, to specify that the sub-document does not include annotations;
* **Geolocation**, a string corresponding to a geographical named entity;
* **Text_Column**, a special entity discussed later;
* **Lat_Long**, for geographical coordinates.

According to the annotation specifications, if the text of a column, with the exception of the first header line, contains completely an annotations **per line**, the corresponding header text is annotated with the corresponding label. In case the line contents of a column contains longer texts containing one or more annotations, the corresponding header text is annotated with **Text_column**, and every line in the column contains its own annotation label.

**Moreover, according to the annotation specifications, contry names, e.g., Nigeria, Tanzania, Italy, are not labelled as geolocations.**

Every annotation label in the dataset is specified by the starting position (integer), the ending position (integer) and the label (string).

