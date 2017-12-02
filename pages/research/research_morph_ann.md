---
title: Morphology annotation
last_updated:
summary: "Morphological annotation of the gold corpus"
sidebar: research
permalink: research_morph_ann.html
folder: research
---
## Morphological annotation of the gold corpus

### Overview

### Annotation format and fields


### Preliminary tests


### Annotation workflow design


### Pre-annotation tool

#### Overview

#### Preliminary dictionary data
To feed our dictionary with forms and associated morphological analysis, we re-used the [JSON output](https://github.com/oracc/json/blob/master/etcsri.zip) of the [ORACC:ETCSRI project](http://oracc.museum.upenn.edu/etcsri/) coupled with an XML harvest of the texts created using xslt. The corpus was first converted to a CoNLL-like format which also served in our [Linked Open Data](/research_lod.html#proof-of-concept) proof of concept.   

From this CoNLL data file, a pseudo CDLI-CoNLL file was created with all unique form and associated morphological sequence with analysis. This was done by combining and re-arranging the data in the columns until the result matched our [CDLI-CoNLL morphology](/cdli_format_cdli-conll.html) columns: FORM, SEGM, and XPOSTAG. The file has around 5000 entries and can be used to populate the pre-annotation tool dictionary to start annotating Sumerian texts. The file is available here *(add the link)*. 

### Validation, storage and conversion


### Annotators




*Émilie Pagé-Perron, Lucas Reckling*
