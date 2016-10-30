ish\_image\_processing
=====
![imagej](https://img.shields.io/badge/ImageJ-macro-orange.svg)
![license](https://img.shields.io/badge/license-apache-blue.svg)

Tools for formatting Marmoset in situ hybridization images


## Requirement
<!--
 - ImageJ
 - Download "Bio-Formats Package" and "Command Line Tools" from [here](http://downloads.openmicroscopy.org/bio-formats/5.1.10/) and put them to ``ImageJ/plugins/``
-->
- Install Fiji
- Add this line to your .bashrc (not necessary but used in the following description): 
```
alias imagej='/Applications/Fiji.app/Contents/MacOS/ImageJ-macosx'
```

## Usage
### ConvertSCNtoTIFF.txt
Converting .scn files to .tif files	\
This macro makes  ``filename.scn_rough.tiff`` from ``filename.scn``.
### 
```
$ imagej -macro ish_image_processing/ConvertSCNtoTIFF.txt [target_directory]
```

### Trimming.txt
Trimming three images for each slide

This macro makes  ``filename.scn_rough-[i].tif`` from ``filename.scn_rough.tif`` where [i] = 1,2,3.
```
$ imagej -macro ish_image_processing/Trimming.txt [target_directory]
```

### Rotate.txt
Rotating each images accuratery

This script updates  ``filename.scn_rough-[i].tif`` , and ignores the slide file ``filename.scn``.
```
$ imagej -macro ish_image_processing/Rotate.txt [target_directory]
```
