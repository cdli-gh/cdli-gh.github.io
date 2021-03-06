---
title: CDLI Image Processing Workflow
sidebar:
 nav: "guides"
permalink: /guides/cdli_images_processing.html
toc: true
---

This page explains how CDLI creates, processes, stores and display digital images. For an extensive overview of the thoughts that have been put in the methods developed to capture and store image data representing cuneiform artifacts, please read "Looking both forward and back: imaging cuneiform" by Jacob L Dahl, Hendrik Hameeuw and Klaus Wagensonner. https://cdli.ucla.edu/pubs/cdlp/cdlp0014_20190319.pdf 

## Images capture
Images can be acquired using different hardware, such as a photo camera, a scanner or a 3D scanner. Below you can find specific instructions in using these various tools for the production of images that can be used or stored by CDLI.


### Scanning artifacts
Scanning cuneiform tablets is a very speedy and cost efficient method for image acquisition. Instructions are temporarilly availeble on CDLI Wiki: http://cdli.ox.ac.uk/wiki/doku.php?id=submission_guidelines#guidelines_for_scanning_tablets


### Photographing tablets and other objects


### Photographing seals method 1: 


### Photographing seals method 2: Turn-table method
Until the CDLN are back online, see a PDF of for a description of Klaus Wagensonner's method
https://www.academia.edu/6997535/Digitizing_in_the_round. This section will be updated based on recent improvements both of hardware and workflow. 

### Photographing seals method 3: 


### Reflectance Transformation Imaging (RTI) Dome

### Photography for photogrametry


### 3D scanning


### Scanning line art


## Processing of images



## Storage of images

### Raw / original files
At this time, CDLI will store raw (generally tiff format) images of scanned tablets, and original photographs. We hope to be able to accept dome raw photos, photos for fotogrametry, and 3d scans raw data, in the future.   

Files should be named according to the artifact they concern and to the acquisition process.  

Anyone interested in storing such images at CDLI should write to us at cdli@ucla.edu  

### Archival files
Archival images are the core images from which all images are derived. They are based on processed raw images. In the case of tablet photos, this involves assembling a tight fatcross, cleaning the background and other adjustement tasks which are outlined in the "Creating fatcrosses" section below. 

#### Creating fatcrosses


#### Archiving line art


#### Archival images storage specifications


### Web images
Web images are processed version of our archival stock in formats optimized for web viewing. 
#### Digital library files arboresence
All our images are shared from the CDLI digital library directory at https://cdli.ucla.edu/dl/. The tree structure of the digital library looks like follows: 

├── lineart
│   └── Pxxxxxx_l.jpg
│   └── Pxxxxxx_ld.jpg
│   └── Pxxxxxx_ls.jpg
├── pdf
│   └── Pxxxxxx.pdf
├── photo
│   └── Pxxxxxx.jpg
│   └── Pxxxxxx_d.jpg
│   └── Pxxxxxx_e.jpg
├── ptm
│   └── Pxxxxxx_o
│       └── x_x.jpg
│   └── Pxxxxxx_r
│   └── Pxxxxxx_x(x(x))
├── svg
├── tn_lineart
│   └── Pxxxxxx_l.jpg
│   └── Pxxxxxx_ld.jpg
│   └── Pxxxxxx_ls.jpg
├── tn_photo
│   └── Pxxxxxx.jpg
│   └── Pxxxxxx_d.jpg
│   └── Pxxxxxx_e.jpg


#### Images types

#### Images quality and size
##### Main images

##### Thumbmails
- The maximum size for trhumbnails is 300 X 800 pixels.
