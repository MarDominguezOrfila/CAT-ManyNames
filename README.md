# CAT-ManyNames

CAT ManyNames is the Catalan version of the ManyNames dataset (https://github.com/amore-upf/manynames), suitable for training Language & Vision models in the task of object naming. The corpus consists of 23,687k images and their corresponding annotations. For an illustration see the images below: 


![image](https://user-images.githubusercontent.com/96442172/175773208-d5be113e-e348-45b8-995a-173ccf9a2341.png)

# Notation


| Abbreviation | Description |
| --- | --- |
|MN	           |ManyNames    |
|VG	           |VisualGenome |
|domain	       |Categorisation of objects into *gent*, *animals_plantes*, *vehicles*, *menjar*, *casa*, *edificis*, and *roba*.

#Data Files
The dataset is provided in a tab-separated text file (.tsv). The first row contains the column labels. Nested data is stored as Python dictionaries (i.e., "{key: value}"). 
The columns are labelled as follows (the most important columns are listed first):
| Column | Type	| Description |
| --- | --- |
| responses |	dict |	Correct responses and their counts |
| topname |	str |	The most frequent name of the object in the largest cluster |
| domain | str  |	The MN domain of the object |
| incorrect |	dict |	Incorrect responses and their counts |
| singletons | dict |	All responses which were given only once and are not synonyms or hypernyms of the topname (these are included in responses) |
| total_responses |	int | Sum count of correct responses |
| split |	str |	Use of the image in *training* vs. *test* vs. *validation* |
| vg_object_id |	int |	The Visual Genome id of the object |
| vg_image_id |	int |	The Visual Genome id of the image |
| topname_agreement | int |	The number of responses for the top name divided by the number of total responses |
| jaccard_similarity | int | Jaccard similarity index of the responses column in CAT_manynames.tsv and human_annotated_testset.tsv |
