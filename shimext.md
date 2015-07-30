---
layout: page
title: ShimExt
excerpt: ShimExt creates a right click menu to rename or copy files with a datestamp.
permalink: /shimext/
---

ShimExt - A Windows datestamp shell utility
===========================================


Features
--------

ShimExt is a right click context menu that provide these file/folder operations:

* Copy the full path of the selected file or folder to the clipboard.
* Copy the selected file or folder to the same folder with a datestamp.
* Rename the selected file or folder with a date stamp.


Example
-------

Example of right-clicking a file named "billings.rtf"...

{:refdef: style="text-align: center;"}
![ShimExt Example]({{ site.baseimg }}/ShimExt/example1.png)
{: refdef}

The selected file or folder can be copied or renamed with an appended date stamp. The date format can be customized.

{:refdef: style="text-align: center;"}
![ShimExt Example]({{ site.baseimg }}/ShimExt/example-copy.png)
{: refdef}


Notes
------

### How the datestamp is determined

* For files, the modified date is used.
* For folders:
    * If the folder contains no files, system time is used.
    * If the folder contains files, the first 5000 files are checked to determine the most recent modifed date.