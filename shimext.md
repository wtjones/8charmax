---
layout: page
title: ShimExt
excerpt: ShimExt creates a right click menu to rename or copy files with a datestamp.
permalink: /shimext/
favicon: shim-icon.ico
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
![ShimExt Example]({{ site.basecdn }}/ShimExt/example1.png)
{: refdef}

The selected file or folder can be copied or renamed with an appended date stamp. The date format can be customized.

{:refdef: style="text-align: center;"}
![ShimExt Example]({{ site.basecdn }}/ShimExt/example-copy.png)
{: refdef}


Notes
------

### How the datestamp is determined

* For files, the modified date is used.
* For folders:
    * If the folder contains no files, system time is used.
    * If the folder contains files, the first 5000 files are checked to determine the most recent modifed date.


Changelog
---------

* 1.0.0 - Initial release
* 1.1.0
    - Allow for multiple file selection.
    - Added "Copy Name to Clipboard" option.
* 1.1.1 - Fixed memory leak in clipboard function.
* 1.2.0
    - Added option to place datestamp before the file name.
    - Added option for stamp attribute: system time/accessed/created
    - MSVC 2012 libraries are now statically linked.
* 1.3.0
    - Periods in folder names are now handled properly.
    - Text month formats (Example: Jun or June instead of 6) now allowed: %b, %B.
    - Default format now has underscore after date.


Download ShimExt (free)
-----------------------

### Prerequisites:

* Windows XP SP3 or greater.
    - Note: If you are running XP, you will need to reboot after upgrading to a new version, although it may not prompt you to do so.

### Download links:
* Download [ShimExt installer msi for 64-bit windows]({{ site.basecdn }}/ShimExt/ShimExt-x64-1.4.0.msi)
* Download [ShimExt installer msi for 32-bit windows]({{ site.basecdn }}/ShimExt/ShimExt-x86-1.4.0.msi)

<form action="https://www.paypal.com/cgi-bin/webscr" method="post">
                    <input type="hidden" name="cmd" value="_s-xclick">
                    <input type="hidden" name="encrypted" value="-----BEGIN PKCS7-----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-----END PKCS7-----
                    ">
                    <input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif" name="submit" alt="PayPal - The safer, easier way to pay online!"
                        style="border: 0px none ; padding: 0px; width: 70px; height: 21px;"> ShimExt is free software, but donations are appreciated to support further development.
                    <img alt="" border="0" src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif" width="1" height="1">
                </form>


  <div id="disqus_thread"></div>
  <script type="text/javascript">
  /* * * CONFIGURATION VARIABLES: EDIT BEFORE PASTING INTO YOUR WEBPAGE * * */
  var disqus_shortname = 'shimext'; // required: replace example with your forum shortname

  /* * * DON'T EDIT BELOW THIS LINE * * */
  (function() {
      var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
      dsq.src = 'http://' + disqus_shortname + '.disqus.com/embed.js';
      (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
  })();
  </script>
  <noscript>Please enable JavaScript to view the <a href="http://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
  <a href="http://disqus.com" class="dsq-brlink">comments powered by <span class="logo-disqus">Disqus</span>
  </a>


<p>Some icons by <a href="http://p.yusukekamiyamane.com/">Yusuke Kamiyamane</a> and <a href="http://glyphicons.com/">Glyphicons Fee</a>. Licensed under a <a href="http://creativecommons.org/licenses/by/3.0/">CC BY 3.0</a>.</p>






