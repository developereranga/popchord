Popchord ships with default values designed to create guitar chords with size of approximately 50 x 100 px. If you want to change this and other options read further.

## Passing Parameters ##

There are two ways of defining custom parameter values.

### 1. **_chordInit()_** Parameters ###

You can pass parameter to _chordInit()_ by supplying a single argument of type javascript object like this:
```
chordInit({nameClass: 'democlass', numString: 7, zoom: 1.7});
```
This call defines class for chord tag as **_democlass_**, sets number of strings to 7 and overall zom to 170% of original size. These parameters affect all chord instances that are initialized by this **_chordInit()_** call. After **_chordInit()_** is called chord images will be initialized with these parameter values for all DOM elements with class **_democlass_** found on the page.

Note that you can pass numeric values either by string ("1.7") or number (1.7). String arguments (such as nameClass) must always be passed as strings.

### 2. DOM Element Attributes ###

With the second method you can define custom attributes to chord _span_ tag like this:
```
<span class="chord" numstring="7", zoom="1.7" chord="">Am7</span>
```
Please note attribute _numstring_ as opposed to chordInit parameter _numString_ - that's because html tags are case insensitive so we might as well have used _numString_ or _NUMSTRING_. Parameter values defined this way apply only to this particular chord.

Note that with this method both string and numeric values must be defined as strings, that's defined by html syntax.

All parameters are listed and their usage explained on Parameters wiki page.

## Error Handling ##

Popchord is designed to fail silently in case of non-fatal error in order not to distract web page viewer by unnecessary alerts. If an invalid parameter value obstructs normal chord image rendering then that image simply won't show up. Examples include invalid number of characters or invalid character in chord definition (**_chord_** parameter).

In case of fatal error all affected chords in the document will be unreadable. Fatal errors are only triggered by **_chordInit()_**, while non-fatal are triggered by chord rendering.

Both error types will throw an exception that can be caught and dealt with accordingly. Errors won't block your javascript code from further execution. They will just stop current call stack from further processing, in other words popchord **_mouseover_** event handler will simply terminate.