---
title: Using CDLI Search
summary: "Complete instructions for using CDLI search"
sidebar: cdli
permalink: cdli_search.html
folder: cdli
---
The CDLI online database contains, as of 1 December 2016, catalogue information for approximately 322,500 cuneiform texts (plus 8,500 entries representing composite texts), 210,000 images, and 2.73 million lines of transliteration and related annotation. Search functions of the website are powered by a MySQL database developed and improved over time by UCLA computer science graduate students Marjan Yahyanejad, Saurabh Trivedi, Oren Freiberg, Stoytcho Stoytchev, Ryan Evans, Eunice Yuh-Jie Chen, Aashith Kamath, Saurabh Trikande, Prashant Rajput, and University of Toronto ANE graduate student Émilie Pagé-Perron.

## Searching the CDLI database

### Simple search

### Advanced search



## Searching the CDLI database prior to Framework Update (2018)
<!--
### Searching the Catalogue
When searching for cuneiform artifacts in the catalogue, it is possible to choose between two basic modes of display.

Full search displays, in the first of three columns, an essentials catalogue, in the second a preferred thumbnail (expandable) of the cuneiform artifact together with hyperlinks to further available images and PDF commentary, and in the third a text transliteration, in some cases with interlinear translations and text comment. Where user search includes transliteration or translation, those items are color coded to simplify their location in the full text. It is possible to cross-search the dataset of transliterations for words and graphemes, limited by period, provenience, etc., as well as to sort results according to catalogue entries.
Tabular search displays a simple table of found texts with essential catalogue information, whereby lead designations (the artificial “P numbers” that identify entered texts and all associated files) link to corresponding full search browse pages with images and transliteration. Where user search includes transliteration or translation, tabular search returns only the line of text containing those items (i.e., defaults to single-line, that are also color coded). Columns in the results pages are sortable by clicking on their respective headers.
CDLI search page defaults to settings for full search; maximally 2000 hits to be displayed per web page, and in the case of transliteration/translation/comment/structure search, our internal counter records in the results header the full number of attestations and the number of texts they are found in. For instance, a search for the Ur III personal name lu2-kal-la currently records a total of 2791 hits in 2512 texts, while displaying the first 2000 of those texts in the first page of the scroll screen; a request of a download of their corresponding full transliterations will, nonetheless, upload to your device a .txt file with all 2512 texts. A conventionalized text designation (preferencing primary publication; if unpublished, consecutively collection/museum number, accession number, and excavation number) is color coded at the top of the full search catalogue results. Clicking on this designation brings up in one archival page the same text with full catalogue, all images and transliteration/translation/comment. Search is exact string, including empty space, and is full-grapheme in transliteration.

Expert users will find our implementation of MySQL regular expressions helpful in complex searches; typing right slashes “/” before and after search string activates regex in catalogue or transliterations; a tutorial of MySQL’s Spencer version of regular expressions is here. For instance, to ensure that a search for texts from the city of Ur results only in Ur entries in provenience, user can enter /^Ur /, thus restricting results to only those entries that begin with Ur and contain a space after, eliminating, for instance, Nippur, Assur, and Uruk.

In the following, we offer short explanations of each search field found in our main searh page. These are individually hyperlinked to their respective search page fields to facilitate quick reference by users.

#### Designation

Please note that our default sort key for search is a calculated field “Designation.” Designation is in fact the lead text ID for all search results (bold and colored at the top of catalogue fields in scroll results) and is usually the same as “Primary publication;” where primary publication is given as unpublished, designation resorts to “Museum number;” where museum number is also unknown, designation moves instead to “Accession number,” and from there to “Excavation number.”

#### Primary publication

Primary publication is conceived to represent what a specialist will usually use to cite a cuneiform artifact. For specialists, as with CDLI, this choice is dictated by the best available visual (line art hand or vector graphic copy, photograph) and/or textual (transliteration, translation, annotation) publication of the artifact, which is understandably not always the initial publication. Preference is also generally given to the appearance of a text in an established series like MVN or ARET, or in such leading journals as JCS or ZA (CDLI’s list of abbreviations is found here). To facilitate system sorting, numerical designations of series or individual texts have been padded with filler zeroes; for instance, not MVN 8, 18, but MVN 08, 018. The best strategy to learn the citation form of a given text is to first type in the series abbreviation, then note and use for successive searches the format of the examples you see. Unpublished artifacts are designated either “unpublished unassigned” or “unpublished assigned,” depending on information we have received from collections managers of their unedited exemplars. We are happy to “assign” unpublished text to named authors where the collection approves of this designation; that author's name is then entered to the Author field in our catalogue. In the case of separate publications of fragments of a single artifact, the best publication of the full piece is chosen; where only partial publications are known, the lead or initial publication is chosen, followed by a plus sign “+”, and successive fragment publications are listed in Secondary publication(s).

Note that special rules apply in the case of several text genres now being entered to CDLI bearing on those texts or text-like artifacts that can be found in multiple copies in antiquity, and that therefore are supplemented with an artificial composite identifier. In the case of literary texts, we have chosen the format “CDLI Literary n,” where n is a six-digit number assigned in the Q catalogue managed by Oracc. Sumerian literary compositions in CDLI were for the most part imported from ETCSL, and are further qualified under subgenre with their common descriptive designations. Similarly, CDLI Lexical n borrows its numerical designations from qcat, and much of its substance from DCCLT. Akkadian, and literary texts of other cuneiform languages, have not been the subject of a systematic online initiative such as that of Oxford’s ETCSL, and are therefore being entered to CDLI based on qcat entries and the designations common in Assyriology. Former designations of text editions, as well as publication designations of individual witnesses, have been relegated to the field Secondary publications (see below). We have not decided whether the well-established text designations assigned within the royal or elite inscription series RIME, RIMA, RINAP and RIMB (supplemented with Nimrud NW Palace for relief inscriptions of Assurnasirpal II’s Northwest Palace) should be treated in the same, generic ‘qcat’ fashion, and have for the time being left the RIME etc. designations in Primary publication. See below for a quick description of the uses of Q-entries in CDLI. Where Q numbers are part of the Primary publication, entries are separated into one artificial “composite” and one or more “witness;” in time, all such texts will be tagged with corresponding Q and line numbers, enabliing the internal creation of score versions of each compilation. Finally, as an integral part of literate Mesopotamia, seals and sealings are recorded in CDLI and designated according to numerical identifiers; in Primary publication, these are found under CDLI Seals n, where n is also a six-digit number taken from our S-catalogue; for an overview, see “CDLI Seals” (short description also below). Primary publication is enabled for MySQL regular expressions.

#### Author(s)

This field is for the name(s) of authors of Primary publications. These names are, with few exceptions, standardized to represent his/her/their full publication name in the form Familyname, Givenname, M.(iddle initial), for instance, Owen, David I. To prevent unnecessary confusion, these full names will be supplied even if some publications used variant forms of an author’s name. We follow authors’ preferences in such cases as Postgate, J. Nicholas. Chinese names dispense with the comma following family names, thus Wu Yuhong. Multiple authors are added following the ampersand “&”, up to three; four or more authors are reduced to Lead Author, et al. Unpublished texts carry the author designation “nn” = nomen nescio (an anonymous or unnamed person [including of unpublished artifacts]). Author(s) is enabled for MySQL regular expressions.

#### Publication date

This should be the actual date given in the copyright page of a monograph, journal series, etc., in which a text was published. “nd” = no date (known to us for a cited publication, or for unpublished texts). Publicaion date is enabled for MySQL regular expressions.

#### Secondary publication(s)

See explanation of Primary publication above. The CDLI field assigned to publication history is currently not systematized, but is being corrected to represent a full citation form of Author, Monograph or Series (year) Numerical designations, for instance, Gadd, Cyril J., UET 6 (1963) 0019. In the case of popular texts, this field can be of distressing size. Note that for the composite text genres mentioned above, publications listed here will in many cases represent the editio princeps of the cited artifacts. Secondary publication is enabled for MySQL regular expressions.

#### Collection

We attempt to cite collections according to their own preferred designations, where possible in their corresponding English forms, including City, (US: State), and Country. In the case of private collections, we give as much information as we know, or are allowed to make public. Collection is enabled for MySQL regular expressions.

#### Accession number

An artifact can receive a variety of identifying designations in the course of moving from ground to collection storage or display. Often, the artifact receives IDs in the field from excavators, then is registered with accession IDs by museums, and is finally assigned a stable collection ID by curators. These are not always widely known, or consistently used identifiers, CDLI catalogue attempts to differentiate between accession and collection IDs, not always successfully. The Kuyunjik (Nineveh) collection of the British Museum has a number of different IDs referring to various excavators (Sm n, Rm n, etc.), to Kuyunjik itself (K n), or as generally with BM pieces, to the date of accession in the museum (1896-06-12, 0035 is the 35th artifact registered on the 12th of June 1896; remember that the same use of zeroes applies as was discussed above under Primary publication). The meaning of collection sigla, usually abbreviations of the museums themselves, is known to specialists, and can usually be deduced from the name found in the “Collection” field. Accession number is enabled for MySQL regular expressions.

#### Collection number

This normally consists of museum siglum + number. The meaning of collection sigla, usually abbreviations of the museums themselves, is known to specialists, and can usually be deduced from the name found in the “Collection” field, but they can also be found in CDLI’s abbreviations pages. Examples are YBC 14389, or VAT 4126. As with publication numbers, many collection numbers contain leading zeros in the database so that records sort properly. In the case of joins of fragments with different collection numbers, the full collection number will be entered for each fragment and will therefore be searchable as exact string. Collection number is enabled for MySQL regular expressions.

#### Acquisition history

The history of artifact acquisition is not well documented in CDLI. Where information concerning past owners, or general excavation records, has been freely available, we have attempted to distill it down to a reasonable narrative and entered it in in free text to Acquisition history (information deemed to be of a private nature is kept in non-public fields). These data can be helpful in cross searching strategies involving artifacts that for whatever reason have moved from one known collection, private or public, to another. Acquisition history is enabled for MySQL regular expressions.

#### Provenience

Where known from excavations, or relatively certain from internal considerations, the provenience of a text artifact is given in the format Ancientname (mod. Modern name), for instance Bābili (mod. Babylon), or Kar-Tukulti-Ninurta (mod. Tulul al-ʿAqir). Where one or the other is not known, or neither, it is signaled with “uncertain.” Provenience is enabled for MySQL regular expressions. Below is a full list of current site names in CDLI catalogue (NB: “Elbonia” indicates our suspicion that an artifact in circulation or in established collections is a modern fake):

Abdju (mod. Abydos, Egypt)
Adab (mod. Bismaya)
Akhetaten (mod. el-Amarna)
Alalakh (mod. Tell Açana)
Alu-eššu (mod. uncertain)
Alu-ša-BAD-MAH-AN (mod. uncertain)
Alu-ša-šuma-ukin (mod. uncertain)
Anšan (mod. Tell Malyan)
Apqu-ša-Adad (mod. Tell Abu Marya)
Arrapha (mod. Kirkuk)
Assur (mod. Qalat Sherqat)
Ba-milkišu (mod. uncertain)
Bābili (mod. Babylon)
Bad-Tibira (mod. Tell Medinah)
Baḫe (mod. uncertain)
Bit-ali-... (mod. uncertain)
Bit-šar-Babili (mod. uncertain)
Bit-ṭab-bel (mod. uncertain)
Bit-zerija (mod. uncertain)
Borsippa (mod. Birs Nimrud)
Der (mod. Tell Aqar)
Dilbat (mod. Deilam)
Dūr-Abī-ēšuḫ (mod. uncertain)
Dur-Katlimmu (mod. Tall Shekh Hamad)
Dur-Kurigalzu (mod. Aqar Quf)
Dur-Šarrukin (mod. Khorsabad)
Dur-Untaš (mod. Chogha Zanbil)
Dusabar (mod. uncertain)
Ebla (mod. Tell Mardikh)
Ecbatana (mod. uncertain)
Ekalte (mod. Tell Munbaqa)
Elbonia ?
Emar (mod. Tell Meskene)
Eridu (mod. Abu Shahrain)
Ešnunna (mod. Tell Asmar)
Garšana (mod. uncertain)
Gasur (mod. Yorgan Tepa)
Girsu (mod. Tello)
Gubla (mod. Byblos)
Ḫarbe (mod. Tell Chuera)
Ḫattusa (mod. Boğazkale)
Hursagkalama (mod. Ingharra)
Huzirina (mod. Sultantepe)
Imgur-Enlil (mod. Balawat)
Irisagrig (mod. uncertain)
Isin (mod. Bahriyat)
Isqalluna (mod. Ashkelon)
Kabnak (mod. Haft Tepe)
Kalhu (mod. Nimrud)
Kanesh (mod. Kültepe)
Kar-bel-matati (mod. uncertain)
Kar-Nabu (mod. uncertain)
Kar-Tukulti-Ninurta (mod. Tulul al-ʿAqir)
Karkemish (mod. Djerabis)
Kazallu (mod. uncertain)
Kilizu (mod. Qasr Shamamuk)
Kish (mod. Tell Ingharra)
Kish (mod. Tell Uhaimir)
Kisurra (mod. Abu Hatab)
Kutalla (mod. Tell Sifr)
Kutha (mod. Tell Ibrahim)
Lagaba (mod. uncertain)
Lagash (mod. El-Hiba)
Larak (mod. Tell Wilayah)
Larsa (mod. Tell as-Senkereh)
Marad (mod. Wanna-wa-Sadum)
Mari (mod. Tell Hariri)
Maškan-šapir (mod. Tell Abu Duwari)
Me-Turran (mod. Tell Haddad)
Nagar (mod. Tell Brak)
Nerebtum (mod. Iščali)
Nigin (mod. Surghul)
Nineveh (mod. Kuyunjik)
Nineveh (mod. Nebi Yunus)
Nippur (mod. Nuffar)
Nuzi (mod. Yorgan Tepa)
Pārśa (mod. Persepolis)
Puzriš-Dagan (mod. Drehem)
Qatara (mod. Tell al Rimah)
Sagub (mod. uncertain)
Šaḫrinu (mod. uncertain)
Samal (mod. Zinčirli)
Shaduppum (mod. Tell Harmal)
Shashrum (mod. uncertain)
Shibaniba (mod. Tell Billa)
Shuruppak (mod. Fara)
Sippar-Amnanum (mod. Tell ed-Der)
Sippar-Yahrurum (mod. Tell Abu Habbah)
Šubat-Enlil (mod. Leilan)
Susa (mod. Shush)
Tarbisu (mod. Tell Sherif Khan)
Terqa (mod. Ashara)
Til Barsip (mod. Tell Ahmar)
Tushhan (mod. Ziyaret Tepe)
Tuttul (mod. Tell Bi'a)
Tutub (mod. Khafaje)
Udannu (mod. uncertain)
Ugarit (mod. Ras Shamra)
Uhaimir-Kish (mod. Tell Uhaimir)
Umma (mod. Tell Jokha)
Upi (mod. Opis)
Ur (mod. Tell Muqayyar)
Urkesh (mod. Tell Mozan)
Uruk (mod. Warka)
Yahrūrum šaplûm (mod. uncertain)
Zabalam (mod. Ibzaikh)
uncertain (mod. Abu Fandowa)
uncertain (mod. Abu Halawa)
uncertain (mod. Abu Jawan)
uncertain (mod. Abu Salabikh)
uncertain (mod. Abu Sêcher)
uncertain (mod. Abu-Maria)
uncertain (mod. Alisar)
uncertain (mod. Amuda)
uncertain (mod. Anatolia)
uncertain (mod. As-Sib)
uncertain (mod. Assyria)
uncertain (mod. Babylonia)
uncertain (mod. Bardi Sanjian Bitwata)
uncertain (mod. Bassetki)
uncertain (mod. Behistun)
uncertain (mod. Ben Shemen, Israel)
uncertain (mod. Beydar)
uncertain (mod. Chagar Bazar)
uncertain (mod. Chogha Mish)
uncertain (mod. Çorum, Turkey)
uncertain (mod. Dharan)
uncertain (mod. Diqdiqqah)
uncertain (mod. Diyala)
uncertain (mod. Dohuk)
uncertain (mod. Dura-Europus)
uncertain (mod. Egypt)
uncertain (mod. Ghazir)
uncertain (mod. Giricano)
uncertain (mod. Godin Tepe)
uncertain (mod. Habuba Kabira)
uncertain (mod. Hadidi)
uncertain (mod. Hazor)
uncertain (mod. Hillah)
uncertain (mod. Himeri)
uncertain (mod. Himrin)
uncertain (mod. Hissar)
uncertain (mod. Ibn Hani)
uncertain (mod. Ibzaih)
uncertain (mod. Indus)
uncertain (mod. Iran)
uncertain (mod. Išān Hāfudh)
uncertain (mod. Jebel Aruda)
uncertain (mod. Jemdet Nasr)
uncertain (mod. Jiroft)
uncertain (mod. Kalah Shergat)
uncertain (mod. Kayseri province)
uncertain (mod. Kermanshah)
uncertain (mod. Lahir)
uncertain (mod. Luristan)
uncertain (mod. Masat Höyük)
uncertain (mod. Mazyad)
uncertain (mod. Megiddo)
uncertain (mod. Mesopotamia)
uncertain (mod. Mugdan)
uncertain (mod. Nar-Madanu)
uncertain (mod. Negub tunnel)
uncertain (mod. Nessana)
uncertain (mod. northern Babylonia)
uncertain (mod. Ortaköy)
uncertain (mod. Ozbaki)
uncertain (mod. Palmyra)
uncertain (mod. Pir Huseyin)
uncertain (mod. Qaṭibat)
uncertain (mod. Rabat Tepe)
uncertain (mod. Samarra)
uncertain (mod. Sealand)
uncertain (mod. Seleucia)
uncertain (mod. Sepphoris)
uncertain (mod. Shadad)
uncertain (mod. Shahr-i Sokhta)
uncertain (mod. Sidon)
uncertain (mod. Sulaima)
uncertain (mod. Syria)
uncertain (mod. Tappeh Bormi)
uncertain (mod. Tell Abu Harmal)
uncertain (mod. Tell Agrab)
uncertain (mod. Tell al-Diba'i)
uncertain (mod. Tell al-Lahm)
uncertain (mod. Tell Dhiba'i)
uncertain (mod. Tell en-Nasbeh)
uncertain (mod. Tell es-Seeb)
uncertain (mod. Tell Fakhariyah)
uncertain (mod. Tell Ghdairife)
uncertain (mod. Tell Hammam et-Turkman)
uncertain (mod. Tell Hammam)
uncertain (mod. Tell Huweish)
uncertain (mod. Tell Jidr)
uncertain (mod. Tell Muhammad)
uncertain (mod. Tell Sabaa)
uncertain (mod. Tell Sifr)
uncertain (mod. Tell Sweyhat)
uncertain (mod. Tell Taban)
uncertain (mod. Tell Ubaid)
uncertain (mod. Tell Uqair)
uncertain (mod. Tell Yarah)
uncertain (mod. Tepe Gawra)
uncertain (mod. Tepe Sialk)
uncertain (mod. Tepe Sofalin)
uncertain (mod. Tepe Yahya)
uncertain (mod. Til-Buri)
uncertain (mod. Uhudu)
uncertain (mod. Umm al-Aqarib)
uncertain (mod. Umm al-Jir)
uncertain (mod. Umm al-Wawīya)
uncertain (mod. Umm Chatil)
uncertain (mod. Umm el-Hafriyat)
uncertain (mod. uncertain)
uncertain (mod. Urartu)
uncertain (mod. Western Iran)
uncertain (mod. Yasuj)
uncertain (modern uncertain)

#### Excavation number

We attempt to follow archaeological conventions in the assignment of excavation numbers to CDLI text artifacts. Such designations can be highly inconsistent. Thus, Uruk/Warka texts are listed, for instance, as W 12345, whereby in early excavations each number represented an artifact “locus” that could itself consist of tens and even hundreds of discrete artifacts. These individual artifacts were, without apparent attention to convention, designated with letters or numbers and sorted alpha-numerically. As with publication numbers, many excavation numbers contain leading zeros in the database so that records sort properly. Excavation number is enabled for MySQL regular expressions.

#### Period

Period designations in CDLI catalogue follow those generally accepted by specialists in cuneiform studies, and consist of a conventional period name followed by approximate dates BC, for instance Uruk III (ca. 3200-3000 BC) or Old Babylonian (ca. 1900-1600 BC). Below is a full list of accepted periods in CDLI:

Pre-Writing (ca. 8500-3500 BC)
Uruk V (ca. 3500-3350 BC)
Uruk IV (ca. 3350-3200 BC)
Uruk III (ca. 3200-3000 BC)
Proto-Elamite (ca. 3100-2900 BC)
ED I-II (ca. 2900-2700 BC)
ED IIIa (ca. 2600-2500 BC)
ED IIIb (ca. 2500-2340 BC)
Ebla (ca. 2350-2250 BC)
Old Akkadian (ca. 2340-2200 BC)
Old Akkadian (ca. 2340-2200 BC)
Linear Elamite (ca. 2200 BC)
Lagash II (ca. 2200-2100 BC)
Harappan (ca. 2200-1900 BC)
Ur III (ca. 2100-2000 BC)
Early Old Babylonian (ca. 2000-1900 BC)
Old Assyrian (ca. 1950-1850 BC)
Old Babylonian (ca. 1900-1600 BC)
Middle Hittite (ca. 1500-1100 BC)
Middle Babylonian (ca. 1400-1100 BC)
Middle Assyrian (ca. 1400-1000 BC)
Middle Elamite (ca. 1300-1000 BC)
Neo-Assyrian (ca. 911-612 BC)
Neo-Elamite (ca. 770-539 BC)
Neo-Babylonian (ca. 626-539 BC)
Achaemenid (547-331 BC)
Hellenistic (323-63 BC)
Parthian (247 BC - 224 AD)
Sassanian (224-641 AD)
Egyptian 0 (ca. 3300-3000 BC)
copy (modern)
fake (modern)
uncertain

Period is enabled for MySQL regular expressions.
#### Dates referenced

Beginning in the Early Dynastic period ca. 2400 BC, Babylonian scribes began to qualify administrative and legal texts with notations clearly identifiable as date designations, consisting of all or some of the categories Ruler, Year of rule, Month of year, Day of month. From the Late Uruk period of the latter third of the 4th millennium BC on, these calendars combined knowledge of solar and lunar cycles to achieve an ideal administrative year of 360 days divided into 12 months of 30 days each. The cultic calender evidently was based on the lunar cycle of ca. 29.5 days for each month, and therefore a lunar year of ca. 354 days and thus the need for intercalation of extra months on average every three years. These dates are currently entered to CDLI catalogue in the form RN.Y.M.D (Royal name is spelled in full with conventional English designations), with “--” for lost information, “00” when information was not given by  the scribe. Month intercalations were designated by scribes with "min," “the second,” or "diri," “extra.” A question mark following a space after the full date notation records doubts about any one, or all of the preceding RN.Y.M.D slots. We are considering expanding our date code to include dynasty/era, as proposed by Oracc. Dates referenced is enabled for MySQL regular expressions.

#### Object type

This gives a general designation of the artifact itself. CDLI’s value list includes tablet, tablet & envelope, bulla, tag, prism, barrel, cylinder, brick, cone, sealing, seal Object type is enabled for MySQL regular expressions.

#### Object remarks

Qualifications of object type can refer to uncommon objects such as stone mace heads, knives, beads, statues, etc. This field also currently includes free text descriptions imported from external sources, and will in time be conventionalized to facilitate a more orderly search procedure. Object remarks is enabled for MySQL regular expressions.

#### Material

The format of material entries is of the type stone: alabaster. Thus, you can search for all objects made of stone, or clay, or metal, but it is also possible to reduce the hits to only those artifacts recorded by us to be made of steatite, but user should note that our files are not complete in this regard. General designations are bitumen, bone (incl. ivory and shell), clay, glass, gypsum (including casts), metal, and stone. “Composite” refers to artificial entries as described above. Artifacts can consist of multiple materials; such hypbrids are then qualified with each, separated by a semi-colon. Material is enabled for MySQL regular expressions.

#### Language

The great majority of entries to CDLI catalogue are qualified by either Sumerian or Akkadian, and we do not currently differentialte between supposed dialects of these two, including the stronger differentiations between northern Assyrian and southern Babylonian Akkadian. Texts containing two or more languages are identified as such, with each language separated by a semi-colon. Pre-Early Dynastic texts (Late Uruk and proto-Elamite) are designated as “undetermined” insofar as their language affiliation is concerned. Below is a full list of currently entered language designations:

Sumerian
Sumerian; Akkadian
Akkadian
Akkadian; Aramaic
Akkadian; Egyptian
Akkadian; Elamite
Akkadian; Elamite
Persian
Akkadian; Elamite; Persian; Egyptian
Akkadian; Persian
Eblaite
Elamite
Harappan
Urartian
Hittite
Hittite; Hattic
Hittite; Hurrian
Hurrian
Phoenician
Ugaritic
Aramaic
Hebrew
Persian
Greek
Sabaean
Mandaic
Egyptian
uncertain
undetermined
no linguistic content
Language is enabled for MySQL regular expressions.

#### Genre

CDLI catalogue needs a general review of its text genre categories. We currently list the following possible designations, that, as in other search fields, can signal the inclusion in one artifact of more than one qualification, each separated by a semi-colon:

Administrative
Royal/Monumental
Votive
Lexical
Lexical; Literary
Lexical; Literary; Mathematical
Lexical; Mathematical
Legal
Letter
Literary
Literary; Mathematical
Omen
Prayer/Incantation
Ritual
School
Mathematical
Astronomical
Scientific
uncertain
fake (modern)
other (see subgenre)
Genre is enabled for MySQL regular expressions.

#### Sub-genre

Sub-genre consists of relatively free text, much of it from legacy data entered to CDLI catalogue in the course of its early compilation. Users should, nonetheless, note several recent changes that are meant to better order royal and literary inscriptions. In the case of Royal/Monumental, sub-genre can consist of “witness” for physical artifacts, and “composite” for the original text or archetype of a given composition. For Sumerian literary texts, CDLI catalogue now lists their corresponding ETCSL designations in sub-genre, while artificial Primary publication designations are being written, namely, “CDLI Literary” followed by the number of Oracc’s Q-catalogue, for instance “CDLI Literary 000751, ex. 010” for the 10th witness to what under sub-genre is called “ETCSL 4.80.02 Kesh Temple Hymn ('Decad no. 06')”. Such designations will eventually be expanded to include all literary texts entered to CDLI catalogue. Sub-genre is enabled for MySQL regular expressions.

#### Composite number

Oracc’s Q-catalogue forms the basis for all cuneiform texts liable to to be found in multiple copies with the exception of seals, thus including royal inscriptions, literary and lexical texts, and a variety of sundry other texts. These Q-designations are of the form Q123456 (Q plus six digits), and can be browsed here. Q-numbers encountered in a search result are hyperlinked to all witnesses and their corresponding composite entry; ideally, only the composite entry will include a translation of the associated ancient text. In a growing number of cases, those Q hyperlinks are followed by a link to “scores” that we are generating from tagged composites and witnesses. Composite number is enabled for MySQL regular expressions.

#### Seal number

Like Q, seal numbers are of the form S123456, that is, S(eal) plus six digits. Seal numbers refer in essence exclusively to physical cylinder or stamp seals, even though we may see that final numbers of seals found only in their impressions on ancient clay artifcats roughly equal those of physical seal artifacts found in existing collections. CDLI work put into seals has been described in two CDLN contributions by Englund and Firth, and Mesopotamian seals are currently the focus of a research project being led by CDLI co-PI Jacob Dahl at the Unmiversity of Oxford. Like Q-numbers, S-numbers encountered in a search result are hyperlinked to all rollings recorded in text artifacts, and to their corresponding composite seal entries. Seal number is enabled for MySQL regular expressions.

#### CDLI number

Artificial designations of CDLI entries in the form of P123456 (as before, P plus six digits) are the core of CDLI text artifact management. P-numbers are unique and are assigned automatically to ever new entry to our catalogue. In turn, all associated files are keyed through these inviolable identifiers, in the form of P123456.atf (transliteration/translation text file), P123456.jpg (archival, usally fatcross photographic image), P123456_l.jpg (archival line art image) and so on. Users can enter P+fewer than six digitls to view sets of texts entered together, for instance P00045 will display all existing entries from P000450 to P000459. CDLI number is enabled for MySQL regular expressions.

#### ATF source

In the same format as used with Author(s), ATF source credits the person or persons who have made electronic transliteratiions available for CDLI ingest. These credit lines are usually not the same as those found in the version histories that accompany all entered transliteration content, since version history records all stages of additions or corrections to the originating files and are done by CDLI-affiliated editors. Steve Tinney offers an ATF primer here, and tools for ATF creation and submission to CDLI may be found here. ATF source is enabled for MySQL regular expressions.

#### Catalogue source

Mostly for internal controls, additions to CDLI catalogue are time-stamped and qualified with designations of persons, offices or projects who have submitted or actually entered new text artifacts to our files. An example is 20150312 cdliadmin_jones, meaning, on 12 March 2015 cdliadmin added to catalogue this entry submitted by “Jones.” Catalogue source is enabled for MySQL regular expressions.

#### Translation source

Interlinear translations are submitted to us, or directly entered to transliteration files by CDLI staff and collaborating specialists; these contributors are cited in the same fashion as that used for Author(s) and ATF source. Translation source is enabled for MySQL regular expressions.


Searching text transliteration, translation and comment

Simple Search of Words or Parts of Words in Transliterations, Translations and Comments

Search in transliterations can be set to locate one or more signs or words in an exact string, or across a full line or text:

Leave at Full or select tabular from the representation menu, and type your search item(s) into the transliteration box, following CDLI ATF-transliteration conventions (š is coded “sz”, emphatics ṣ and ṭ are coded “s,” and “t,”, and ḫ is simple “h”; for further conventions, see the ATF conventions pages used by CDLI and Oracc).
ATF editing characters, for instance “#” to indicate a damaged sign, or “!” to indicate an emendation, are ignored in default setting of CDLI search.
Optional: Restrict the search by typing additional conditions into the catalogue fields.
Hit your keyboard’s return, or click on the search button at the end of the page to initiate your search.
We have recently implemented a similar search functionality for lines of translation and comment that follow lines of text transliteration, as well as for text structure. As of 18 Masrch 2015, there are 58,500 lines of translated cuneiform text in CDLI files, mostly in English but some instances of German, French, and even Catalan; 15,100 lines of interlinear annotation, from comment on sign preservation up to decimal calculations that underlie numbers in accounts, and 90,000 lines of (usually formulaic) comment to text structure. The great bulk of current CDLI translations comprises those created by Daniel Foxvog for the Mesopotamian Royal Inscriptions component of the website, but we anticipate more translation content of Sumerian literary texts as ETCSL migrates to CDLI. For the record, CDLI restricts translation of texts liable to appear in multiple witness artifacts to their artificial composite entries. As with transliteration search, the exact string of searched characters in translations and comments are highlighted in blue to facilitate their discovery within the texts. Exact string in these instances means that, for example, a search for “pig” will display that string as a discrete word, but also all uses of “pigs”, “pigherder” and so on. Only “pig” will be highlighted.

In all three instances, you will receive a list of occurrences that offers you some options for further discovery:

In tabular search, click on the column headers to sort according to those catalogue criteria.
You may further expand your results to show full transliterations and available images and image links by clicking on the corresponding hyperlink above your search results. In the case of multiple item transliteration search, you may also expand the results to display all instances of full text transliterations that included searched items somewhere in the text, not just in one line.
If more occurrences have been found than are displayed, click on the next page link above or below the results to see the remaining items.
Some Useful Explanations of the Simple Search Procedure

When searching for words or parts of words in the transliterations, you should be acquainted with the ATF conventions that apply to all texts in the CDLI. For our purposes, we may refer to Oracc’s C(anonical)-ATF as “CDLI ATF”; its main points are:

Sign values in Sumerian must conform to the set of CDLI values; see this download page and contact cdli@ucla.edu if you have questions or recommendations concering the sign readings or names listed there.
readings not assigned indices by Borger, <i>MZL</i>, must be followed by ‘x’ (the letter lowercase ex) and a description of the sign using sign names in upper case, for instance sudx(|SU.KUR|).
Never put brackets inside graphemes: write ab# not [a]b.
For purposes of qualifying state of preservation, both simple and complex signs are considered atoms; thus, a component of a complex sign such as |UR2x(A.HA)| is never qualified as damaged or broken, only the whole sign. Similarly, a damaged number notation, for instance [5(disz)]+4(disz) must be coded as 9(disz)#.
Never put logograms in capitals: only uninterpreted sign names, and complex signs are in upper case in CDLI ATF.
For logograms in non-Sumerian texts use underscores and lower case, i.e., write %a _lugal_, not %a LUGAL.
For logograms where the logogram language is not Sumerian, use a language switch after the underscore: (%hit ...) \_%a mu-u2\_.
All numbers must be qualified (3(disz), 4(u) etc.) <strong>except</strong> sexagesimal numbers in Place Value notation (PVN).
The only ATF protocols that are allowed in CDLI ATF are: #atf: lang XXX, where XXX is a language code; #atf: use math, where PVN is to be used.
The #-sign (“hash”-sign) introduces comments about individual line content and always follows the commented line.
The $-sign introduces comment of text structure, never of line content.
$-lines for breakage of uncertain length must conform to the following patterns: $ broken (for instances of loss of full surface or column); $ beginning broken (after this, use primes on subsequent line numbers but where the length of the break is known, instead enter all line numbers and use [...] for the line content; beginning broken may also refer to some unknown number of columns missing, after which the first preserved column is to be qualified @column 1' and so on); $ rest broken (see above for both missing lines and columns); $ n lines broken (within column and surface; line numbering after resumption of preserved text is in sequence with the number preceding the break with, for example, 5'. following either 4. or 4'.).
Special conventions apply to the proto-cuneiform texts; since all ‘Sumerian’ readings of the Late Uruk texts may be debated, we provisionally consider them unknown but apply common sign names, in upper case, to the characters, where indicated by unclear variants qualified with a tilde ~ and an alphanumeric string, usually just ~a, ~b etc. Numerical notations are transliterated according to the sign list ATU 2 and conventions described in Damerow & Englund, ATU chapter 3, for instance 3(N01). We have provisionallty added some few ad hoc qualifiers, for instance 4(N01@f) for the flattened N01 forms of the Archaic Ur texts, or 1(N01~t) for pre-writing clay counters, so-called tokens, found in bullae assemblages.
Examples in CDLI ATF (and see here for further quick pointers):

##### Example 1

&P100003 = AAS 015
\#atf: lang sux
\@tablet
\@obverse
1. 1(disz) geme2 u4 1(disz)-sze3
2. ki dingir-ra-ta
3. da-da-ga
4. szu ba-ti
@reverse
$ blank space
1. mu ki-masz{ki} ba-hul

The various ATF features illustrated here are:
The &-line: Every text begins with an &-line giving the ID and the text’s designation according to the CDLI catalogue; if you believe your text is not yet in the catalogue, e-mail cdli@ucla.edu to get the ID and designation or to have one entered by us.
\#atf: lang sux: You can specify the main language for the text; for Akkadian just write #atf: lang akk.
@tablet: You can specify an object type; this is normally @tablet, but others include @bulla and @envelope. If an object type which is used in the CDLI catalogue is not understood by the ATF processor, you can use the exactly equivalent form @object OBJECT_TYPE, e.g., @object brick.
@obverse, @reverse: You can specify the part of the object you are transliterating; the edges are given using: @left @right @top @bottom (but note that no physical surface of a tablet is to be included in CDLI ATF unless it, such as @left or in the case of occasional partial sums at the bottom of colums in Ur III administrative texts, assumes an explicit function in text format).
Lines of text: Lines of text are for the most part just like regular Assyriological practice. See Example 2 for how to do breakage.
Determinatives are given in curly brackets: Phonetic complements and glosses are marked with a + immediately after the first curly bracket; they are assumed to be in the same language as the rest of the word.
Rulings and Blank Spaces: Lines ruled on the tablet as paragraph separators, as well as empty space or space used for seal impressions, can be marked with $-lines (“dollar-lines”).
Numbers: All numbers are qualified.
Example 2

&P348658 = SpTU 2, 055
\#atf: lang akk
@tablet
@obverse
1. t,up-pi _a-sza3_ ki-szub-ba#-[a ...]
2. {i7}har-ri sza2 {d}muati? x [...]
3. sza2 qe2-reb unu#[{ki}]

Damage and breakage:

There are no half-brackets in ATF: signs that are damaged are flagged with the hash-sign (#) after the grapheme.
Signs that are completely broken away are placed in square brackets; square brackets may not occur inside a grapheme, only before or after it. The ellipsis (...) may be used to indicate that an undeterminable number of signs are missing.
Signs that cannot be identified are transliterated as x; when a number is missing the convention is to use n; further qualification of n as n(disz), n(u) etc. is allowed.
Querying, Correction and Collation:

The other flags are the query (?) which can be placed after a grapheme to indicate uncertainty of reading; the asterisk (\*) can indicate a collated reading (but is to be voided when the version history indicates CDLI confidence in the transliteration); and the exclamation mark that indicates editor correction. After a corrected sign, the actual sign on the tablet may optionally be given, using sign names in upper case: a! or ki!(DI).
It is useful to understand how the simple search procedure works.
Searching for words:

A word has to be written as a set of one or more graphemes separated by dashes. Determinatives (semantic or phonetic glosses such as “d” = “divinity”, “ki” = “place”) are to be enclosed in curly brackets { and }. The special character “š” in upper or lower case (Š, š) is coded in CDLI ASCII with “SZ” and “sz”, respectively. There is no special character for “ḫ” that is either “H” or “h”.
CDLI search .
Subsequently, searches are performed on the transliterations of these tablets in order to identify the lines containing the word searched for.
Finally, the designations of the found tablets are displayed together with transliterations of the lines containing this word.
Searching for parts of words:

Searching for an individual grapheme will result in precisely those lines containing this grapheme. For instance, searching for lu2 (human) as part of a word will find all tablets with the word lu2, but also, e.g., lu2-kal-la (an official at Umma) or lu2-u18 (“mankind”). Honoring of exact string in CDLI search does afford users the option of bounding search for the word lu2 by typing in a space before and after the sign reading (NB: line returns are treated in search as spaces)—this will, however, exclude such examples as lu2-ra, “to the man”, etc.
Searching for part of a word consisting of a sequence of graphemes will result in a list of tablets that contain this sequence.
Search Tips

Servers invariably experience periods of high traffic, or software breakdowns that cause a website to slow down or break apart. We regularly monitor CDLI for such interruptions, but are grateful for user reports of problems.
We are working to normalize all sign readings in CDLI, but we deal with quite a lot of legacy transliterations with varying standards. You therefore might want to search independently for “gisz”, “gesz”, and “GISZ” to find all occurrences of the grapheme. Similarly, since the archaic texts (ca. 3400-2700 BC) are coded according to standards of the Uruk Project and the sign list ATU 2, you have to search independently for “dug”, “DUG~a”, “DUG~b”, etc. Case-sensitive search can be activated in search settings under Transliteration to ensure only instances of DUG(~a/b/c; tilde in Late Uruk sign designations are treated like dashes), but also of later entry of DUG to indicate uncertainty about the correct reading of the sign, or for instance in lexical syllabaries to indicate a “sign name”.

-->
