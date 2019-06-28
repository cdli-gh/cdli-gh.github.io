---
title: MTAAC Research Process >> Text Selection
permalink: /research/research_select_corpus.html
sidebar:
  nav: "research"
toc: true
---
## Selection criteria
In order to prepare the required texts for the gold corpus, a selection must first be made to ensure an adequate repartition of texts based on various criteria, such as:

- provenience of text (distribution)
- length of text (distribution)
- number of columns (distribution)
- ~500 translated texts in total
- least fragmentary possible

These criteria have been defined based on ongoing discussions between E. Pagé-Perron,  C. Chiarcos, I. Khait, L. Reckling and R. K. Englund.


## Extracting potential candidates from the database

In order to generate a list with additional information about the texts from which to choose, we first extracted transliterated public texts with the required information for identifying and classifying the texts.

The following MySQL query was applied to the production database of the CDLI on December 21th 2017. [The corresponding datafiles](https://github.com/cdli-gh/data/tree/a4a35127eb84f1898986b7eb7efe45bf4868b136) are available in the CDLI data folder under the corresponding commit of that date.

```
SELECT c.id_text, f.wholetext, c. period, c.collection, c.width, c.thickness, c. height, c.provenience, c.primary_publication, c.dates_referenced FROM fulltrans f, cataloguesnew c WHERE f.object_id = c.id_text AND c.period IN ('Ur III (ca. 2100-2000 BC)' , 'Ur III (ca. 2100-2000 BC) ?') AND f.wholetext > '' AND c.genre IN  ('administrative', 'legal', 'letter') AND c.public = 'yes' AND c.public_atf = 'yes' AND language = 'Sumerian'
```

In English this translates as "select these data fields from those two database tables, based on the fact that they have a transliteration, that they are of the specific targeted period and genres, that they are indeed written in the Sumerian language and that they are public entries".

This results in a selection of 70,333 texts in total.

The resulting data was extracted in TSV format and is available in the [gold corpus repository](https://github.com/cdli-gh/mtaac_gold_corpus/tree/master/scripts/gold_corpus).


## Analyzing the data to provide more information








*Émilie Pagé-Perron, Ilya Khait*
