yasSlide
========

Div Background  slideshow with pre-loading of images and auto resizing

A really simple div background slideshow jquery plugin using CSS3 transitions for a smooth fade between slides and only 4k in size and no dependencies on other libraries apart from jQuery.

Images are loaded pre-emptively and only displayed once loaded (especially useful if site is being viewed on slow data connection).

*How does it work?*

Simple. Create a div, populate an array with your files and then call yasslide - it's as easy as that!

*Example*

<pre>
&lt;!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"&gt;
&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;head&gt;
&lt;meta http-equiv="Content-Type" content="text/html; charset=utf-8" /&gt;
&lt;title&gt;Untitled Document&lt;/title&gt;
&lt;style&gt;
html { height:100%; }
body { position:absolute; top:0; bottom:0; right:0; left:0; background:#09F;padding:0;margin:0;overflow:hidden;}
#footer {position:relative;bottom: 0; left:0; width:100%;height:60px;background:#666;}
#header {position:relative;top: 0; left:0; width:100%;height:60px;background:#666;  float-left;}
#content {position: relative;height: 100%;padding:0;margin:0;}
&lt;/style&gt;
&lt;script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"&gt;&lt;/script&gt;
&lt;script src="js/yasslide.js"&gt;&lt;/script&gt;
&lt;script&gt;
$(document).ready(function(){
	$('#content').height($('body').outerHeight()-$('#header').outerHeight()-$('#footer').outerHeight()-21);
  files=['http://myserver.com/images/slide01.jpg','http://myserver.com/images/slide02.jpg','http://myserver.com/images/slide03.jpg'];
  $('#content').yasslide({
		   delay: 3000,  // optional - delay in milli-seconds
		   files: files, // an array of image files
		   debug: true, //optional - output messages to console.log
		   //top: '0px' optional - depending on your container div, where to create the floating div.  try without first.
		   });
});
&lt;/script&gt;
		&lt;/head&gt;

&lt;body&gt;
&lt;div class='wrapper'&gt;
    &lt;div id='header'&gt;Header Text&lt;/div&gt;
    &lt;div id='content'&gt;&lt;/div&gt;
    &lt;div id='footer'&gt;Footer Text&lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

For further examples see <a href="http://yasslide.chris-backhouse.com">yasslide.chris-backhouse.com</a>

changes 0.0.4 - pass new array of files on resize.
				new options for background-posiiton and background-size
				
