---
title: Morphology annotation
sidebar:
  nav: "research"
permalink: /research/research_morph_ann.html
toc: true
---
## Morphological annotation of the gold corpus

### Overview

We will manually annotate 5.2% of the total corpus, around 4,000 texts, with morphological and lexical information. 20% of these texts will be accompanied by English translations, the remainder will be untranslated. These 4,000 or so texts will constitute our gold corpus.

To facilitate the manual annotation process, ATF transcriptons of the gold corpus are converted to a version of the CoNLL-U format specialized for our corpus, known as CDLI-CoNLL. CDLI-CoNLL is designed to ease data entry and store lexical and morphological data. Once converted, transcriptions are arranged in a table with one word per row and columns for morphological and lexical data. The CDLI-CoNLL files will live separately from but alongside the ATF in the CDLI database.


### Annotation format and fields

The CDLI-CoNLL tables contain the following columns:

* ID:  Information about the surface, column, line, and word token, in the format o.col1.1.1 = first column, first line first word. Information about the column can be omitted if the text does not have columns (o.1.1).

* FROM:  The token from the text, i.e. ATF transcription.

* SEGM:  A normalized form of the token using the dictionary form of the word as the stem.

* XPOSTAG:  Morphological tags following ORACC ETCSRI. Morphological tags are separated by periods, surrounding a stem tagged with the part of speech. Implicit morphemes are added in square brackets.

### Preliminary tests


### Annotation workflow design


### Pre-annotation tool

The job of the annotators is to fill in the SEGM and XPOSTAG columns with the appropriate lexical and morphological information. Manual annotation is assisted by a [pre-annotation tool](https://github.com/cdli-gh/morphology-pre-annotation-tool). Taking into account existing annotated texts, the pre-annotation tool will automatically populate unambiguous fields in the CDLI-CoNLL table. It may also make suggestions in additional columns to the right of those normally included in CDLI-CoNLL. In these cases, annotators select the best choice and copy/paste it into the appropriate column. Then annotators fill in any remaining blanks.

Because the pre-annotating tool bases its suggestions on extant annotated texts, it is initially trained on the ETCSRI corpus, whose language only partially overlaps with that of the Ur III administrative corpus. Thus at first the pre-annotating tool will populate relatively few fields, but as Ur III texts are added to the pre-annotator its dictionary will learn more relevant data and will in turn populate more fields.


#### Preliminary dictionary data
To feed our dictionary with forms and associated morphological analysis, we re-used the [JSON output](https://github.com/oracc/json/blob/master/etcsri.zip) of the [ORACC:ETCSRI project](http://oracc.museum.upenn.edu/etcsri/) coupled with an XML harvest of the texts created using xslt. The corpus was first converted to a CoNLL-like format which also served in our [Linked Open Data](/research_lod.html#proof-of-concept) proof of concept.   

From this CoNLL data file, a pseudo CDLI-CoNLL file was created with all unique form and associated morphological sequence with analysis. This was done by combining and re-arranging the data in the columns until the result matched our [CDLI-CoNLL morphology](/cdli_format_cdli-conll.html) columns: FORM, SEGM, and XPOSTAG. The file has around 5000 entries and can be used to populate the pre-annotation tool dictionary to start annotating Sumerian texts. The file is available here *(add the link)*.

### Validation, storage and conversion


### Annotators
Morphology annotators for the MTAAC projects are Lucas Reckling, William McGrath, Jinyan Wang, Émilie Pagé-Perron, Ilya Khait, Heather D. Baker, and Robert K. Englund.




*Émilie Pagé-Perron, Lucas Reckling*
