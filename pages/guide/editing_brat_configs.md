---
title: Editing brat Configurations
keywords:
tags:
sidebar: guide
permalink: /editing_brat_configs.html
summary:
---

### Editing Brat Annotation Configurations in annotation.conf ###
Detailed instructions for editing brat configurations can be found here: http://brat.nlplab.org/configuration.html

annotation.conf is one of four configuration files used by Brat and defines the annotations tags themselves. Other .conf files define the visual aspects of brat (visual.conf), annotation tools (tools.conf), and keyboard shortcuts for speedy annotating (kb_shortcuts.conf).

annotation.conf is divided into sections with the headers

```
[entities]
[relations]
[events]
[attributes]
```

Define entities in a list, one item per line:

```
[entities]
ENTITY1
ENTITY2
ENTITY3
```

Relations between entities can be defined as follows:

```
[relations]
relation_name Arg1:<ENTITY>; Arg2:<ENTITY>
```

This allows for relations between any two entities. The arguments can be further specified to include only certain entities:

```
nsubj Arg1:<NOUN>; Arg2:<VERB>
```

This disallows syntactically meaningless relations from being annotated by mistake, but is more time consuming to define.

In our current relations configuration, we are using `<TOKEN>` in place of `<ENTITY>` for defining relations, inserting the line `<TOKEN>=<ENTITY>`:

```
[relations]
<TOKEN>=<ENTITY>
acl	Arg1:<TOKEN>, Arg2:<TOKEN>
advcl 	Arg1:<TOKEN>, Arg2:<TOKEN>
```

***When attempting to do the same with events and attributes, using `<TOKEN>=<ENTITY>` did not work, however this could be a coding error on my part. According to the [brat guide](http://brat.nlplab.org/configuration.html#additional-details), custom macros should work across the board.

Events are defined like entities but with the possibility of linking additional entities (or events) to that event in the format `ROLE:TYPE`, where `ROLE` can be freely defined:

```
[events]
#to tag a sale and identify the participants
Sale Buyer:<ENTITY>, Seller:<ENTITY>

#to tag an event with a single participant
Published_a_tablet Scholar:<ENTITY>
```

After tagging the event, dragging from the event label to an entity label will allow the user to specify the relevant participants within the event

Attributes can be easily defined for entities and events, but as of Oct. 13 2017 I have not been able to figure out if attributes may be assigned to a relation itself (e.g. tag a proleptic genitive relation as such).

The syntax for defining attributes is as follows:

```
[attributes]
#single-valued
Name_of_attribute Arg:<ENTITY/EVENT>
#multiple values
Name_of_Attribute Arg:<ENTITY/EVENT>, Value:V1|V2|V3|etc
```

brat includes defined “shortcuts” for enhanced usability:
```
<ENTITY>
<RELATION>
<EVENT>
 <ANY> (= any type)
 ```

These macros can be define at will, as with `<TOKEN=<ENTITY>`

### Editing Brat Keyboard Shortcut Configurations in kb_shortcuts.conf ###
The annotation process can be facilitated by the use of keyboard shortcuts assigned to annotation tags. These shortcuts are defined in kb_shortcuts.conf by a single hotkey and its associated annotation:

```
N	NUM
V	VERB
S	nsubj
```

In order to use a shortcut one still must manually select an entity or relation, but the shortcut will replace manual selection within the resulting window. Keyboard shortcuts work with entities, relations, and events, but not with attributes.


To actually update the configurations in brat, access the CDLI-DEV server and go to /Library/WebServer/Documents/cdli/brat/data/ and then into the appropriate folder (make sure you start from the root, not users; the current folder we’re configuring for tests is /Library/WebServer/Documents/cdli/brat/data/cuneiform).

Transfer the new configuration file to dev server and replace the extant one (save a copy before major changes). Refresh brat to test changes; syntax errors will quickly display on the bottom of the screen when the configs are loaded.

### Embedding a brat visualization ###

The following steps will allow a brat visualization to be embedded as an .svg image file:

1. Use Brat to annotate text sample as desired.
2. Click “data” and select “svg" under the “Export” heading
3. View source of resulting page
4. copy source into text editor, excluding the first line (source should begin with <svg… and end </svg>)
5. save with extension .svg
6. add your .svg image file to the MarkDown document as normal using

In case of “serious error,” try deleting the .stats_cache file (invisible) and refreshing brat
