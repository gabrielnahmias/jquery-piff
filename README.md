PIFF
=============

**PIFF** (**P**DF **I**nline **F**ormatting **F**unction) is a **jQuery _plugin_** that quickly makes any link to a PDF forcefully viewed in a window.

[Link soon!  Live version is a prototype.](#)

What does it do?
-----------

* Loads linked PDFs in either a nice modal window (includes five themes to choose from) or with the browser.
* Removes the need to load stylesheets separately (it does all this on its own).
* Makes everyone around you cream.

How to use it
-----------

Before doing anything, you must include **jQuery** (I could append it to the ```head``` with the script.  Hmm...) and **jquery.piff.js** (or the minified version, **jquery.piff.min.js**) on your page like so
	
```javascript
<script language="javascript" src="//ajax.googleapis.com/ajax/libs/jquery/1/jquery.min.js" type="text/javascript"></script>
<script language="javascript" src="jquery.piff.js" type="text/javascript"></script>
```

Now that that huge achievement is accomplished, we can move right on to the simple shiz.

There are five main options you can set; however, for the window object, refer to the link below:

1.  **cssDir** (default: "css") - the directory the CSS (and related images) for PIFF will be stored.
2.  **dir** (default: "") - a string to prepend before the URL path (i.e., http://www.google.com/DIR/etc/).
3.  **exceptions** (default: null) - a regular expression you can use to exclude certain matching HREFs.
4.  **modal** (default: true) - modal (can be ```"fancybox"``` [be sure to include the appropriate files for this], ```true``` for colorbox, or ```false``` or popup window).
5.  **theme** (default: none) - the name of a theme to load (from the path specified by cssDir).  The format of a PIFF theme CSS file is **NAME.css**.  **NOTE:** don't include **.css** when specifying this option (i.e., to change the theme to "elegant", you simply set it as such).
6.  **window** (default: false) - an object containing settings for the window to be opened.  See <a href="http://www.jacklmoore.com/colorbox">this page</a>.

Examples
-----------

As simple as it gets (no options specified and without selector [selects all anchor tags whose HREF ends with .pdf]):

```javascript
$.piff();
```

Some fun options:

```javascript
$("a.pdf").piff( {
	
	theme: "sharp"
	
	window: {
		
		height: 300,
		
		onClose: function() { alert("You just ruined my life."); console.warn("I'm hacking your computer."); },
		
		width: 500
		
	}
	
} );
```

Browser support
-----------

* Google **Chrome**
* Mozilla **Firefox** 3+
* IE9
* Others as of yet untested (help me out!)

License
-----------

Public domain

Acknowledgements
------------

PIFF is a project by [Gabriel Nahmias](http://github.com/terrasoftlabs "Terrasoft's GitHub"), co-founder of Terrasoft.
