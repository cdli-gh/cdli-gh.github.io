---
title: morphology
sidebar: guide
permalink: /guide_morphology.html
folder: guide
summary: 
---

## Morphology annotation

We will manually annotate 5.2% of the total corpus, about 4,000 texts, with morphological and lexical information. 20% of these texts will be accompanied by English translations, the remainder will be untranslated. These 4,000 or so texts will constitute our gold corpus. 

To facilitate the manual annotation process, ATF transcriptons of the gold corpus are converted to a version of the CoNLL-U format specialized for our corpus, known as CDLI-CoNLL. CDLI-CoNLL is designed to ease data entry and store lexical and morphological data. Once converted, transcriptions are arranged in a table with one word per row and columns for morphological and lexical data. The CDLI-CoNLL files will live separately from but alongside the ATF in the CDLI database.

The CDLI-CoNLL tables contain the following columns:

* ID:  Information about the surface, column, line, and word token, in the format o.col1.1.1 = first column, first line first word. If the text does be omitted if the text does not have columns (o.1.1).

* FROM:  The token from the text, i.e. ATF transcription.

* SEGM:  A normalized form of the token using the dictionary form of the word as the stem.

* XPOSTAG:  Morphological tags following ORACC ETCSRI. Morphological tags are separated by periods, surrounding a stem tagged with the part of speech. Implicit morphemes are added in square brackets.

The job of the annotators is to fill in the SEGM and XPOSTAG columns with the appropriate lexical and morphological 
Manual annotation is assisted by a [pre-annotation tool](https://github.com/cdli-gh/morphology-pre-annotation-tool). Taking into account existing annotated texts, the pre-annotation tool will automatically populate unambiguous fields in the CDLI-CoNLL table. It may also make suggestions in additional columns to the right of those normally included in CDLI-CoNLL. In these cases, annotators select the best choice and copy/paste it into the appropriate column. Then, annotators fill in any remaining blanks.

Because the pre-annotating tool bases its suggestions on extant annotated texts, it is initially trained on the ETCSRI corpus, whose language only partially overlaps with that of the Ur III administrative corpus. Thus at first the pre-annotating tool will populate relatively few fields, but as Ur III texts are added to the pre-annotator its dictionary will learn more relevant data and in turn populate more fields.


## Morphological Annotation Guide

The following is a step-by-step guide to annotating .conll files. It has been tested for a streamlined annotation experience.

### 0. Install and Prepare The Morphological Pre-Annotation Tool (MPA)

The MPA must be installed before use. Instructions for installation as well as running the tool can be found here: https://github.com/cdli-gh/morphology-pre-annotation-tool

*Note: it may be easiest to create a new folder from the root in order to simplify file pathways while using the MPA*

Upon installation, run the tool using the folder of the ETCSRI training corpus to create a dictionary (annotated_morph_dict.json). After running, the second line from the bottom should read "creating annotation json dictionary file as," followed by a file pathway to annotated_morph_dict.json. Open annotated_morph_dict.json using Atom or a similar text-editor to confirm its structure is correct (FORM: [[SEGM1	XPOSTAG1], [SEGM2	XPOSTAG2]]):

```json
{
  "pisan-dub-ba": [["bisajdubak", "N"]], 
  "hu-hu-nu-ri{ki}": []
}
```

If the dictionary appears copacetic then the MPA is ready for use with the Ur III corpus.

**Do not move the dictionary file.**

### 1. Run the Pre-Annotation Tool

Before new texts can be manually annotated they must be pre-annotated by the MPA. For the best result, annotators will update their local dictionaries based on all annotated files. To do this:

1. Retrieve fresh copies of all annotated files from WHEREVER THEY ARE BY WHATEVER MEANS and place them in a folder
2. Delete annotated_morph_dict.json 
3. Run the MPA on the folder of annotated texts
4. Check to see that a new annotated_morph_dict.json file has been created and appears correct, as above

Texts to be annotated will be parcelled out to annotators in .conll format. To pre-annotate the texts, simply run the MPA on the folder of texts to be annotated.

_

### 2. Complete the Pre-Annotated Texts

In order to ensure that the format of the .conll files remains intact, they will be annotated using a spreadsheet. [LibreOffice](https://www.libreoffice.org/), an opensource office suite, was selected for this purpose because it can open .conll files without having to fiddle with the extensions.

To edit the .conll files, open LibreOffice and start a new spreadsheet, then open the file. LibreOffice will open the file in text editing mode as a default if it is opened on the main screen. When LibreOffice opens a .conll file, a dialog box will in will appear (pictured below). Make sure to check ONLY the “tab” option as a separator. This ensures that the proper formatting is preserved the files are edited. 

![](https://cdli-gh.github.io/images/ma_guide/LibreOfficePrompt1.png)

The sheet should look like this:

![](https://cdli-gh.github.io/images/ma_guide/LibreOfficeSpreadsheet.png)

Human annotators will be responsible for filling in the SEGM and XPOSTAG columns, which contain a normalization of the token given in the FROM column and house ORACC/ETSCRI morphological tags, respectively. Pre-annotated .conll files will open with some of the SEGM and XPOSTAG fields already populated thanks to MPA, but these must be manually checked for accuracy and corrected accordingly. In some cases, the field will be blank but MPA will have made suggestions in an additional column. Human annotators may choose the appropriate option from the suggestions. The remainder of the blank SEGM and XPOSTAG fields will be completed manually.

#### 2.1 Completing the SEGM Column

The SEGM column contains a normalization of the token given in the FROM column.

#### 2.2 Completing the XPOSTAG Column

The XPOSTAG column houses ORACC/ETSCRI morphological tags. Morphological tags are separated by periods, surrounding a stem tagged with the part of speech (POS). Implicit morphemes are added in square brackets.

ORACC/ETCSRI morphological tagset can be found here: [LINK TO COME]

The POS tagset can be found here: [LINK TO COME]


### 3. Save

Saving will prompt a dialog box from LibreOffice about file formats (pictured below). It is VERY important that the files are formatted correctly to avoid extra steps. Choose “use CSV.” You can uncheck the box at the bottom, which will disable this prompt in the future.

If you are NOT prompted with this dialog box while saving, check your first file by opening it in a text-editor like Atom. A properly formatted .conll file should appear columned in Atom as it did in LibreOffice. If it this is not the case, something has gone wrong. Double-check that the file was imported with only the “tab” separator option selected.

### 4. Run the Pre-Annotation Tool Again

When the last text in a group is complete, MPA must be run one more time to update the dictionary before moving on.
