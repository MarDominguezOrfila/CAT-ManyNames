# CAT ManyNames

CAT ManyNames és la versió en català de ManyNames (https://github.com/amore-upf/manynames) adequat per entrenar models de llenguatge i visió en la tasca de "object naming". El corpus consta de més de 23.000 imatges i les seves corresponents anotacions. Per a un exemple vegeu les imatges següents:

*CAT ManyNames is the Catalan version of the ManyNames dataset (https://github.com/amore-upf/manynames) suitable for training Language & Vision models in the task of object naming. The corpus consists of more than 23K images and their corresponding annotations. For an illustration see the images below:*


![image](https://user-images.githubusercontent.com/96442172/175773208-d5be113e-e348-45b8-995a-173ccf9a2341.png)

# Human-annotated test set

El "human-annotated test set" s'ha creat per avaluar la qualitat del CAT ManyNames. El seu corpus consta de 1.072 imatges i les seves corresponents anotacions (aproximadament 10 anotacions per imatge).

*The Human-annotated test set has been built to evaluate the quality of the CAT ManyNames dataset. Its corpus consists of 1,072 images and their corresponding annotations (ca. 10 annotations per image).*

# Notació / Notation


| Abbreviation | Description |
| --- | --- |
|MN	           |ManyNames    |
|VG	           |VisualGenome |
|domain	       |Categorisation of objects into *gent*, *animals_plantes*, *vehicles*, *menjar*, *casa*, *edificis*, and *roba*.


# Fitxers de Dades / Data Files

El CAT ManyNames i el *Human-annotated test set* es proporcionen en un fitxer de text separat per tabulacions (.tsv). Les primeres files contenen els noms de les columnes. Les dades jerarquitades s'emmagatzemen com a diccionaris de Python (és a dir, "{key: value}").

Els noms de les columnes són els següents (les columnes més importants estan enumerades primer):

*The dataset and the human-annotated test set are provided in a tab-separated text file (.tsv). The first rows contain the column labels. Nested data is stored as Python dictionaries (i.e., "{key: value}"). 

The columns are labelled as follows (the most important columns are listed first):*

|Column             |Type	 |Description |
| --- | --- | --- |
|*responses* |	dict |	Correct responses and their counts |
|*topname*            |	str  |	The most frequent name of the object in the largest cluster |
|*domain*             | str  |	The MN domain of the object |
|*incorrect* (not avalilable for the human-annotated test set)         |	dict |	Incorrect responses and their counts |
|*singletons* (not available for the human-annotated test set)        | dict |	All responses which were given only once and are not synonyms or hypernyms of the topname (these are included in responses) |
|*total_responses*    |	int  | Sum count of correct responses |
|*split*              |	str  |	Use of the image in *training* vs. *test* vs. *validation* |
|*vg_object_id*       |	int  |	The Visual Genome id of the object |
|*vg_image_id*        |	int  |	The Visual Genome id of the image |
|*topname_agreement* (only available for the test split) | int  |	The number of responses for the top name divided by the number of total responses |
|*jaccard_similarity* (only available for the test split)| int  | Jaccard similarity index of the responses column in CAT_manynames.tsv and human_annotated_testset.tsv |
|*raw_responses* (only available for the human annotated test set)| dict | Responses before being corrrected and filtered and their counts |

# Com citar el CAT ManyNames / Citing CAT ManyNames

# Informació addicional / Additional information

CAT ManyNames té una llicència Creative Commons Attribution 4.0 International License.
Aquest projecte ha estat recolçat per la unitat de Text Mining del Barcelona Supercomputing Center.

*CAT ManyNames is licensed under a Creative Commons Attribution 4.0 International License. 
This project was supported by the Text Mining unit at the Barcelona Supercomputing Center.*

