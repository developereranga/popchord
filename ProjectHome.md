# Popchord #
Displays guitar (or other fretted string instrument) chord diagrams on a web page. This is useful for making chords-lyrics pages of popular songs or any other page where you want to show guitar chords. When mouse pointer is moved over a DOM element that has certain class a guitar chord diagram image is showed above that DOM element. Popchord uses inline **_svg_** vector graphics that is supported by all major modern browsers (please see **Tested With** section below).

# How to Use It #
To use popchord you need to edit html code in plain text editor. There are three simple things that need to be done:

### 1. Include the Library ###
Insert the following line somewhere in the **_head_** section of your web page:
```
<script src="popchord-1.0.js"></script>
```
### 2. Enclose All Chord Names in html Tags ###
This should be **_span_** or other inline html tag and you must assign it attributes **_class_** and **_chord_**. For example:
```
<span class="chord" chord="x02010">Am7</span>
```
Value of the **_chord_** attribute represent chord in the following manner:
```
x - string not played
0 - empty string
1-9,a-f - fret number (hexadecimal number to allow maximum of 15 frets)
```
### 3. Initialize Chords ###
Call function **_chordInit()_** somewhere on web page, either from javascript code or **_body_** tag, such as:
```
<body onload="chordInit()">
```
If you call **_chordInit()_** from javascript code make sure to call it after receiving page load event otherwise chords may not be properly initialized.

That's all you need to do, everything else is done automatically by popchord library. If you want to know about advanced features like parameter tweaking or error handling please read Wiki pages.

This library is used on http://bossanovaguitar.com website. If you use popchord on your site and want it listed here please leave a note.

# Tested with #

|![http://www.w3schools.com/images/compatible_firefox.gif](http://www.w3schools.com/images/compatible_firefox.gif)|![http://www.w3schools.com/images/compatible_ie.gif](http://www.w3schools.com/images/compatible_ie.gif)|![http://www.w3schools.com/images/compatible_chrome.gif](http://www.w3schools.com/images/compatible_chrome.gif)|![http://www.w3schools.com/images/compatible_opera.gif](http://www.w3schools.com/images/compatible_opera.gif)|![http://www.w3schools.com/images/compatible_safari.gif](http://www.w3schools.com/images/compatible_safari.gif)|
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
|Firefox                                                                                                          |IE                                                                                                     |Chrome                                                                                                         |Opera                                                                                                        |Safari                                                                                                         |

### Donate ###
If you use popchord on your website please consider small donation to help us supporting and maintaining this library.

<a href='https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=DAC3Q9MKWABB6'>
<img src='https://www.paypalobjects.com/en_US/i/btn/x-click-butcc-donate.gif' /></a>