---
title: Morphology
sidebar:
  nav: "guides"
permalink: /guides/guide_morphology.html
toc: true
---




## MTAAC’S Approach to Sumerian Morphology

The model of Sumerian morphology employed at MTAAC approximates that developed by Gabor Zólyomi, a model demonstrated at the ETCSRI project, and articulated in Zólyomi’s 2017 grammar. Some conventions relating to word categorization and tag sets  invite explanation: i) according to this model, Sumerian adjectives do not constitute a distinct word class. Instead, they are analyzed as non-finite verbal forms; ii) infinitives and participles, morphologically indistinct from other non-finite forms, are not distinguised; iii) a non-finite verbal form without a suffix is marked as tenseless (or absolute), and a null morpheme is supplied. Non-finite forms consisting of STEM + .a are marked as preterite. Non-finite forms consisting of STEM + .ed are marked as present-future.


## Morphological Annotation Guide

The following is a step-by-step guide to annotating .conll files. It has been tested for a streamlined annotation experience.

### 0. Install and Prepare the Morphological Pre-Annotation Tool (MPA)

The MPA must be installed before use. Instructions for installation as well as running the tool can be found here: https://github.com/cdli-gh/morphology-pre-annotation-tool

*Note: it may be easiest to create a new folder from the root in order to simplify file pathways while using the MPA*

Upon installation, run the tool using the folder of the ETCSRI training corpus to create a dictionary (annotated_morph_dict.json). After running, the second line from the bottom should read "creating annotation json dictionary file as," followed by a file pathway to annotated_morph_dict.json. Open annotated_morph_dict.json using Atom or a similar text-editor to confirm its structure is correct (FORM: [[SEGM1	XPOSTAG1], [SEGM2	XPOSTAG2]]):

```json
{
  "pisan-dub-ba": [["bisajdubak", "N"]],
  "hu-hu-nu-ri{ki}": []
}
```

If the dictionary appears all right then the MPA is ready for use with the Ur III corpus.

**Do not move the dictionary file.**

### 1. Run the Pre-Annotation Tool

Before new texts can be manually annotated they must be pre-annotated by the MPA. For the best result, annotators will update their local dictionaries based on all annotated files. To do this:

1. Retrieve fresh copies of all annotated files from (add repository link) and place them in a folder
2. Delete annotated_morph_dict.json
3. Run the MPA on the folder of annotated texts
4. Check to see that a new annotated_morph_dict.json file has been created and appears correct, as above

Texts to be annotated will be parcelled out to annotators in .conll format. To pre-annotate the texts, simply run the MPA on the folder of texts to be annotated.

_

### 2. Complete the Pre-Annotated Texts

In order to ensure that the format of the .conll files remains intact, they will be annotated using a spreadsheet. [LibreOffice](https://www.libreoffice.org/), an opensource office suite, was selected for this purpose because it can open .conll files without having to fiddle with the extensions.

To edit the .conll files, open LibreOffice and start a new spreadsheet, then open the file. LibreOffice will open the file in text editing mode as a default if it is opened on the main screen. When LibreOffice opens a .conll file, a dialog box will appear (pictured below). Make sure to check ONLY the “tab” option as a separator. This ensures that the proper formatting is preserved as the files are edited.

![](https://cdli-gh.github.io/images/ma_guide/LibreOfficePrompt1.png)

The sheet should look like this:

![](https://cdli-gh.github.io/images/ma_guide/LibreOfficeSpreadsheet.png)

Human annotators will be responsible for filling in the SEGM and XPOSTAG columns, which contain a normalization of the token given in the FROM column and house ORACC/ETSCRI morphological tags respectively. Pre-annotated .conll files will open with some of the SEGM and XPOSTAG fields already populated thanks to MPA, but these must be manually checked for accuracy and corrected accordingly. In some cases, the field will be blank but MPA will have made suggestions in an additional column. Human annotators may choose the appropriate option from the suggestions. The remainder of the blank SEGM and XPOSTAG fields will be completed manually.

#### 2.1 Completing the SEGM Column

The SEGM column contains a normalization of the token given in the FROM column.

#### 2.2 Completing the XPOSTAG Column

The XPOSTAG column houses ORACC/ETSCRI morphological tags. Morphological tags are separated by periods, surrounding a stem tagged with the part of speech (POS). Implicit morphemes are added in square brackets.

The ORACC/ETCSRI morphological tagset can be found here: [LINK TO COME]

The POS tagset can be found here: [LINK TO COME]


### 3. Save

Saving will prompt a dialog box from LibreOffice about file formats (pictured below). It is VERY important that the files are formatted correctly to avoid extra steps. Choose “use CSV.” You can uncheck the box at the bottom, which will disable this prompt in the future.

If you are NOT prompted with this dialog box while saving, check your first file by opening it in a text-editor like Atom. A properly formatted .conll file should appear columned in Atom as it did in LibreOffice. If this is not the case, something has gone wrong. Double-check that the file was imported with only the “tab” separator option selected.

### 4. Run the Pre-Annotation Tool Again

When the last text in a group is complete, MPA must be run one more time to update the dictionary before moving on.
