#Bug Magnet

Exploratory testing assistant for Chrome. Adds common problematic values and
edge cases to the context menu (right-click) for editable elements, so you can
keep them handy and access them easily during exploratory testing sessions.

##Usage

The easiest way to install the extension is from the [Chrome Web
store](https://chrome.google.com/webstore/detail/efhedldbjahpgjcneebmbolkalbhckfi). After
installation, just right-click on any editable item on the page and you'll see a
Bug Magnet submenu. Click an item there, and it will be inserted into the
editable field. 

Alternatively, you can load the extension from the source files - see _Running
from a local setup_ below.

##Features

* Convenient access to common boundaries and edge cases for exploratory testing
* Works on input fields, text areas, content editable DIVs
* Works on multi-frame pages, but only if they are from the same domain
* Only works in Chrome
* Tiny overhead per page (<1k), no 3rd party library dependencies, completely passive, so it does not interfere with your web app execution in any way

##Questions, suggestions

Twitter: [@gojkoadzic](http://twitter.com/gojkoadzic)

##Resources for more info

* [E-mail address test cases](http://blogs.msdn.com/b/testing123/archive/2009/02/05/email-address-test-cases.aspx)
  * [Dot atoms in e-mail](http://serverfault.com/questions/395766/are-two-periods-allowed-in-the-local-part-of-an-email-address)
  * [Interactive RFC e-mail validation](http://isemail.info/)
* [Falsehoods Programmers Believe About Names](http://www.kalzumeus.com/2010/06/17/falsehoods-programmers-believe-about-names/)
  * [We have an employee whose last name is Null](http://stackoverflow.com/questions/4456438/how-can-i-pass-the-string-null-through-wsdl-soap-from-actionscript-3-to-a-co)
  * [Animal rights activist changes name to GoVeg.com](http://usatoday30.usatoday.com/tech/webguide/internetlife/2003-08-01-goveg_x.htm)
  * [Longest English surname on record](http://en.wikipedia.org/wiki/Leone_Sextus_Tollemache)
* [Elisabeth Hendrickson's test heuristics cheat sheet](http://testobsessed.com/wp-content/uploads/2011/04/testheuristicscheatsheetv1.pdf)

##Customising

You can add your own values to the right-click menu by modifying
[config.json](src/config.json). The format is simple:

* a hash object property is a sub-menu
* a String property is a menu item. The property name is used as a menu item label 
  and the value is inserted into the text field on click.
* an Array property is a sub-menu, allowing you to quickly add a list of Strings
  without a special label (the element values are used both as menu labels and
  as text to insert).

###Running tests

Install Grunt, Node and NPM (instructions are in [GruntFile.js](GruntFile.js)). Then run tests
from the command line using

    grunt jasmine

###Running from a local setup

Load [manifest.json](src/manifest.json) from the **src** folder in Chrome as an [unpacked
extension](https://developer.chrome.com/extensions/getstarted#unpacked).



##Icon credit

Magnet icon from [Woothemes Ultimate Icon Set by Nishan Sothilingam](http://iconfindr.com/1vSsaKB)
