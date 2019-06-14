---
title: Tagsets
sidebar:
  nav: "guides"
permalink: /guides/guide_tagsets.html
toc: true
---

## POS tags
ORACC: <http://oracc.museum.upenn.edu/doc/help/languages/akkadian/index.html>  (scroll down to half the page) 


ETCSL: <http://etcsl.orinst.ox.ac.uk/edition2/etcslhelp.php#pos> 



UD: <http://universaldependencies.org/docs/en/pos/all.html>  


Penn: <https://www.ling.upenn.edu/courses/Fall_2003/ling001/penn_treebank_pos.html>


|ORACC||ETCSL||UD||Penn Treebank POS|
|:---|:---|:---|:---|:---|:---|:---|:---|:---|
|AJ|adjective (including statives)|AJ|adjective|ADJ|adjective|JJ|Adjective|7|
|||||||JJR|Adjective, comparative|8|
|||||||JJS|Adjective, superlative|9|
|AV|adverb|AV|adverb|ADV||RB|Adverb|20|
|||||||RBR|Adverb, comparative|21|
|||||||RBS|Adverb, superlative|22|
|NU|number|NU|numeral|NUM|Numeral|CD|Cardinal number|2|
|CNJ|conjunction|C|conjunction|CONJ|coordinating conjunction|CC|Coordinating conjunction|1|
|DET|determinative pronoun|PD|pronoun/determiner|DET|determiner|DT|Determiner|3|
|||||||EX|Existential there|4|
|||||||FW|Foreign word|5|
|J|interjection|I|interjection|INTJ|interjection|UH|interjection|26|
|||||||LS|List item marker|10|
||
|||||||NNS|Noun, plural|13|
|N|noun (including statives)|N|noun|NOUN|Noun|NN|Noun, singular or mass|12|
|||||PART|particle|PRT|particle|(chunk tags)|
|||||||PRP|Personal pronoun|18|
|||||||POS|Possessive ending|17|
|PP|possessive pronoun|||||PRP$|Possessive pronoun|19|
|||||||WP$|Possessive wh-pronoun|35|
|||||||PDT|Predeterminer|16|
|||||SCONJ|subordinating conjunction|IN|Preposition or subordinating conjunction|6|
|||||||NNPS|Proper noun, plural|15|
|||||PROPN|Proper noun|NNP|Proper noun, singular|14|
|||||SYM|symbol|SYM|Symbol|24|
|||||||TO|to|25|
|||||||VBZ|Verb, 3rd person singular present|32|
|V|verb (including infinitives, marked with EPOS 'N and gerundive GW)|V|verb|VERB|Verb|VB|Verb, base form|27|
|||||||VBG|Verb, gerund or present participle|29|
|||||||VBP|Verb, non-3rd person singular present|31|
|||||||VBN|Verb, past participle|30|
|||||||VBD|Verb, past tense|28|
|||||||WRB|Wh-adverb|36|
|||||||WDT|Wh-determiner|33|
|||||||WP|Wh-pronoun|34|
|||ADP|adposition|
|||AUX|auxiliary verb|
|IP|independent/anaphoric pronoun|
|DP|demonstrative pronoun|
|MOD|modal, negative, or conditional particle|||||MD|Modal|11|
|PRP|preposition|
|QP|interrogative pronoun|
|RP|reflexive/reciprocal pronoun|
|REL|relative pronoun|
|SBJ|subjunction|
|XP|indefinite pronoun|
|||NEG|negator|
|||||PUNCT|punctuation|
|||||X|Other|

## Named Entities
ORACC: <http://oracc.museum.upenn.edu/doc/help/languages/propernouns/index.html>  

ETCSL: <http://etcsl.orinst.ox.ac.uk/edition2/etcslhelp.php#propernouns>  


|Named Entities (ORACC/ETCSL)|
|ORACC||ETCSL||
|:---|:---|:---|:---|
|DN|Divine Name|DN|divine name|
|EN|Ethnos Name|EN|ethnic name|
|GN|Geographical Name*|GN|geographical name|
|MN|Month Name|MN|month name|
|ON**|Object Name|ON**|other name|
|PN|Personal Name|PN|personal name|
|RN|Royal Name|RN|royal name|
|SN|Settlement Name|SN|settlement name|
|TN|Temple Name|TN|temple name|
|WN|Watercourse Name|WN|watercourse name|
|AN|Agricultural (locus) Name|
|CN|Celestial Name|
|FN|Field Name|
|LN|Line Name (ancestral clan)|
|QN|Quarter Name (city area)|
|YN|Year Name|

* Lands and other geographical entities without their own tag.  
** Note the different usages of the ON tag.

## Morphological tags

### Morphological tags comparative chart
[Morphology chart under development](https://docs.google.com/spreadsheets/d/1y0_y9HDQNwH0VqDCjjYuUpFsugw4GEybu6Pu01I_D9c/edit#gid=0)

The ablative's function of distributive is not distinguished in the two sets.

### ETCSL Morphological tags
The ETCSL morphological tags mostly give a normalization that can then be treated with rules to disambiguate meaning. Exception is made for the verbal bases which are explicitly identified (aspect, plural, etc).

- Creating Tools for Morphological Analysis of Sumerian [Link to the pdf](https://gate.ac.uk/sale/lrec2006/etcsl/etcsl-paper.pdf)

Some examples:

POS|form|normalized
----|----|-----
N|kur-kur-ra-gin7|L,ak.gin
N|cag4-gada-la2-be2-e-ne|L,bi.ene
V|L,ani.ak|hul2-la-ni-a
V|mu.ra.I.n:L|e-ri-in-bar-re-ec
V|ga.V.n.ci:L|ga-an-ci-gen
V|ha.ba.NI.n:L|ha-ba-ni-in-dug4

The tags seems to only appear on words that display affixes (the absolutive is not marked).


For a full description of the morphological annotations system, see the ETCSRI website. URL

The ETCSRI morphological tagging is very explicit and consists of three different attributes:
1. The morpheme column based on logical table of possible suites of morphemes
2. The usage of the morphemes
3. the normalized form of the text

Attributes 2 and 3 are used in our CoNLL-U annotation in a hybrid attribute, eg:
> iri-kug-ga-ka-ni

Original
> N1=Irikug.N5=ak.N3=ani.N5=ø  
> N1=NAME.N5=GEN.N3=3-SG-H-POSS.N5=ABS  
> Irikug.ak.ani.ø  

MTAAC modified version
> Iriku=NAME.ak=GEN.ani=3-SG-H-POSS.ø=ABS

Missing affixes are added in the morphology, eg. nin-a-ni becomes
> N1=nin.N3=ani.N5=ra  
> N1=STEM.N3=3-SG-H-POSS.N5=DAT-H  
> nin.ani.ra  

or

> nin=STEM.ani=3-SG-H-POSS.ra=DAT


The morphological tags are explicit and give information not only about the morpheme at hand but hint at the construction of the whole verbal chain. Eg:

morpheme|tag|meaning
----|----|-----
enden|1-PL-A|first person plural agent suffix
enden|1-PL-S|first person plural subject suffix (df)
enden|1-PL|first person plural suffix in plural transitive preterite verbal forms


Or give indications about subtleties in meaning

morpheme|tag|meaning
----|----|-----
e|DAT-NH|non-human dative case-marker
e|L3-NH|non-human locative3 case-marker

*Émilie Pagé-Perron*
