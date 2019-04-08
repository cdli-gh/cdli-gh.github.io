---
title: "Sumerian manual annotation workshop"
sidebar:
  nav: "guides"
permalink: /guides/guide_annotation_workshop.html
toc: true
---

<!--
Salutations and thanks, first time!;
overview of workshop:
hands on, practical
-->

## Introductions

- Émilie Pagé-Perron
- Ilya Khait
- Jinyan Wang
<!-- background, role;-->
- "Tour-de-table"
<!-- background, technical, sumerian; -->


## Principles

- What are linguistic annotations?
- What are possible types of linguistic annotations?

- How does one parse Sumerian in class?

1. dingir-mah
en: For Dingirmaḫ,
2. e2-IGI-NIM-pa-e3
en: E’iginimpa’e,
3. ensix(|GAR.PA.TE.SI|)
en: ruler
4. adab{ki}
en: of Adab,
5. e2-mah mu-na-du3
en: built (her temple) the Emah


- Familiarity with ORACC lemmatizaton?
http://oracc.museum.upenn.edu/doc/help/lemmatising/primer/

- What are the downsides of this system?
- How to add syntax, and semantic annotations?

<!-- talk about that more during talk -->
The MTAAC manual annotation pipeline has been designed to satisfy two criteria:

1) facilitate machine ingestion of the texts

<!-- - part of MTAAC w specific objectives
- data spacity challenge, increase repetition/ more patterns to pick-up
- practical and democratically used formats -->

2) make the annotation process as fast as possible

<!-- - not necesserilly user friendly
    interface
    learning curve
    installtion
- Tools def can be reused ands improved for other projects
- will be integrated in the enw cdli website as services
- Stuggle to annotate fast:
  - still working on the tagset, eg why stem reduplicated? -->

## Basics

### Repos
#### Most useful
- Morphologically annotated texts https://github.com/cdli-gh/mtaac_gold_corpus (morph/to_dict)
- Annotation dashboard https://github.com/cdli-gh/annotation_assistant
- ATF2CoNLL converter https://github.com/cdli-gh/atf2conll-convertor
- Morphological pre-annotator https://github.com/cdli-gh/morphology-pre-annotation-tool 
<!-- Ilya will expalin its principles -->


#### Other resources
- New Framework (for advanced developpers only) https://gitlab.com/cdli/framework
- CDLI data dump https://github.com/cdli-gh/data
- Documentation website https://github.com/cdli-gh/cdli-gh.github.io (https://cdli-gh.github.io/)

### Other links
- Brat server : http://173.230.166.232/brat/#/ann_test/ cdli_syntax:split-ergative (login: hover in top right corner)

### CDLI search and downlaod
<!-- useful until at least the end of the summer
talk about the new interface @ talk  -->

- how do you use CDLI?
- advanced search overview  https://cdli.ucla.edu/search/
- search aid page https://cdli.ucla.edu/?q=cdli-search-information

- testing out (find texts that have a transliteration AND a translation)
- download ATF (look at atf format a bit later)

### Tagsets
MTAAC POS & NE (ORACC Original) https://docs.google.com/spreadsheets/d/1Is7MGG0h8h0vfHj9C9mnWOD2utPeuvm1ZeYb1dsaejg/edit?usp=sharing
ETCSRI MORPH (original) http://oracc.museum.upenn.edu/etcsri/parsing/index.html
MTAAC MORPH  https://docs.google.com/spreadsheets/d/1y0_y9HDQNwH0VqDCjjYuUpFsugw4GEybu6Pu01I_D9c/edit?usp=sharing

Shared tagsets :
Unimorph https://docs.google.com/spreadsheets/d/1B-S8-t6mo1QQOog2-r4KqwGeRW7fyTC1dm6c-OIGmY4/edit?usp=sharing 
Universdal Dependencies (convertion for morphology, straight up for syntax https://universaldependencies.org/

### Data formats
ATF
https://cdli-gh.github.io/assets/texts⁩/P102341.atf
https://cdli-gh.github.io/assets/texts⁩/P340403.atf

cdli-CoNLL
https://cdli-gh.github.io/assets/texts⁩/P102341.conll
https://cdli-gh.github.io/assets/texts⁩/P340403.conll

CoNLL-U:  Universal dependencies tags

Brat: not for humans!  http://brat.nlplab.org/standoff.html

RDF http://www.lrec-conf.org/proceedings/lrec2018/pdf/862.pdf (p5.)

### Dashboard


### Pre-annotator
Ilya : 
- How does the pre-annotator of morphology work?
- Demonstration

  
### Manual annotation
Jinyan :

https://cdli-gh.github.io/assets/texts⁩/pre-annotated⁩/P102341.conll
https://cdli-gh.github.io/assets/texts⁩/pre-annotated⁩/P340403.conll

- How to work with a pre-annotated text
- Demonstration of decision making in the annotation phase
- Participants try morphological annotation

## Syntax
Ilya : 
- How does the pre-annotator of syntax work?
    - How does shift-reduce works?
- Demonstration



List:

https://docs.google.com/document/d/1jgH0rtV-33hN-EL9JAqDcTaUtyBe3RP6HkP1I4JOx0A/edit


Shift-reduce rule example :
( Genitive, rune #17 )


- How would we go about to create rules for the agent/subject/object syntactic roles?




### Manual annotation
Brat
Pseudo brat in the 


Example :
http://173.230.166.232/brat/#/ann_test/text2019_5


Hi and thanks 
Overview of what we will be doing
Jinyan and Ilya to introduce themselves
Intro about the basic principles and objectives of the annotation
can be extended to more later
Part of a project with specific objectives

Where to find stuff
Open access to some of the google docs
Documentation website
The repos
the links will be there so they can refer back
then showing them how to get a text from cdli
and provide them with pre-annotated texts
so they dont have to run the pre-annotator
I thnk there I would explain how the pre-annotator works
and let jinyan explain how to work with a pre-annotated text
then you can put me on and I can tell:
(1) how the morph. pre-annotation tool works 
(2) how the syntax pre-annotation tool works
and demonstrate it


## Activities

- Create a [Github account](https://github.com/join)
- Install [Atom](https://flight-manual.atom.io/getting-started/sections/installing-atom/)
- Install the [annotation assistant](https://github.com/cdli-gh/annotation_assistant)
- Edit morphologically pre-annotated texts (using the annotation helper or a standalone pre-annotated file available [here](https://cdli-gh.github.io/assets/texts⁩/) )
- Upload your own text to [Brat](http://173.230.166.232/brat/#/ann_test/) and try it out
