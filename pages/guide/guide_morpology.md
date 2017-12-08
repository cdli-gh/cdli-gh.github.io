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

Because the pre-annotating tool bases its suggestions on extant annotated texts, it is initially trained on the ETCSRI corpus, whose language only partially overlaps with that of the Ur III administrative corpus. Thus at first the pre-annotating tool will populate relatively few fields, but as Ur III texts are added to the annotated it will in turn



# The Morphological Pre-Annotation Tool (MPA)

The MPA must be installed. Instructions for installation as well as running the tool can be found here: https://github.com/cdli-gh/morphology-pre-annotation-tool

Upon installation, run the tool using the folder of the ETCSRI training corpus to create a dictionary (annotated_morph_dict.json). After running, the second line from the bottom should read "creating annotation json dictionary file as," followed by a file pathway to annotated_morph_dict.json. Open annotated_morph_dict.json using Atom or a similar text-editor to confirm its structure is correct (FORM: [[SEGM1	XPOSTAG1], [SEGM2	XPOSTAG2]]):

```json
{
  "pisan-dub-ba": [["bisajdubak", "N"]], 
  "hu-hu-nu-ri{ki}": []
}
```

If the dictionary appears copacetic then the MPA is ready for use with the Ur III corpus.

The following is a step-by-step guide to annotating .conll files. It has been tested for a streamlined annotation experience:

1. Open the .conll file using LibreOffice.

Open LibreOffice and start a new spreadsheet, then open the .conll file from here. LibreOffice will open the file in text editing mode as a default if it is opened on the main screen. When you open a .conll file using LibreOffice, a dialog box will in will appear. Make sure to check ONLY the “tab” option as a separator. This ensures that the proper formatting is preserved as we edit the files. 



Your sheet should look like this:

2a. For non-pre-annotated .conll files, complete the SEGM and XPOSTAG fields.

The SEGM column contains a normalization of the token given in the FROM column.

The XPOSTAG column houses ORACC/ETSCRI morphological tags. Morphological tags are separated by periods, surrounding a stem tagged with the part of speech (POS). Implicit morphemes are added in square brackets.

ORACC/ETCSRI morphological tagset can be found here:
The POS tagset can be found here:

To assist in this process, we extracted the extant morphological annotation data from the ETCSRI corpus. Since we are

2b. For pre-annotated .conll files, verify the populated SEGM and XPOSTAG fields and fill in the blanks.

Pre-annotated .conll files should open with many of the SEGM and XPOSTAG fields already populated by our pre-annotation tool. These must be manually checked for accuracy and corrected accordingly. In some cases, the field will be blank but the pre-annotation tool will have made suggestions in an additional column. Human annotators may choose the appropriate option from the suggestions. The remainder of the blank SEGM and XPOSTAG fields can be completed in the same manner as 2a.

3. Save.
Saving will prompt a dialog box from LibreOffice about file formats. It is VERY important that our files are formatted correctly to avoid extra steps. Choose “use CSV.” You can uncheck the box at the bottom, which will disable this prompt in the future.

If you are NOT prompted with this dialog box while saving, check your first file by opening it in a program like Atom. A properly formatted .conll file should appear columned in Atom as it did in LibreOffice. If it this is not the case, something has gone wrong. Double-check that the file was imported with only the “tab” separator option selected.

Annotating TL;DR:
1. Open the prepared .conll file in LibreOffice.
2a. If blank, complete the SEGM and XPOSTAG fields.
2b. If pre-annotated, double-check populated fields and fill in the blanks.
3. Save
