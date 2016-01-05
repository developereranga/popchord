# Parameters #

Some parameters make no sense in **_chordInit()_** (like **_chord_**) while others make no sense as DOM attribute (like **_nameClass_**). Please note that for regular DOM properties (colors, font, etc.) you can use any valid CSS syntax.

### 1. Parameters Allowed Only in **_chordInit()_** Call that are Mapped to Corresponding CSS Property ###

  * **nameClass** - chord name DOM element's class (default: 'chord', CSS property **_class_**)
  * **colClass** - chord name color (default: '#0040FF', CSS property **_color_**)
  * **cursorClass** - cursor shape used when mouse is over chord name (default: 'pointer', CSS property **_cursor_**)
  * **fontweightClass** - chord name font weight (default: 'bold', CSS property **_font-weight_**)

### 2. Parameter Allowed Only as DOM Attribute ###

  * **chord** - chord definition (default: 'xxxxxx' - this means that if you don't specify chord definition you'll get empty fretboard image)

### 3. Parameter Allowed in Both Calls ###

  * **colHilite** - chord name color used when mouse pointer is over chord name (default: '#FF3030')
  * **width** - fretboard width in px (default: 40)
  * **aspect** - aspect ratio of fretboard (default: 1.8)
  * **marginTop** - top margin (default: 2)
  * **marginBottom** - bottom margin (default: 7)
  * **marginLeft** - left margin (default: 2)
  * **marginRight** - right margin (default: 2)
  * **marginEmpty** - top/bottom margin of empty string circle symbol (default: 2)
  * **marginNum** - left/right margin of fret number shown for chords starting or ending above **_numFret_** fret(default: 1.5)
  * **numFret** - number of frets shown(default: 4)
  * **numString** - number of strings (default: 6)
  * **thickFret** - fret line thickness in px (default: 1.5)
  * **thickFret1st** - 1st fret line thickness in px (default: 3)
  * **thickString** - string line thickness in px(default: 0.6)
  * **thickEmpty** - empty string circle symbol line thickness in px (default: 1)
  * **capFret** - fret linecap style (default: 'round')
  * **capString** - string linecap style (default: 'square')
  * **radDot** - radius of dot circle represented as percentage of maximum allowed radius which is defined by one half of distance between adjacent strings (default: 85)
  * **radEmpty** - radius of empty string circle represented as percentage of maximum allowed radius same as above (default: 60)
  * **colBG** - graphics background color (default: '#ffffff')
  * **colFretboard** - fretboard color (default: '#ffffff')
  * **colFont** - fret number font color (default: '#000000')
  * **colDot** - dot circle color (default: '#000000')
  * **colFret** - fret color (default: '#000000')
  * **colString** - string color (default: '#000000')
  * **fontSize** - fret number font size as percentage of distance between frets (default: 75)
  * **fontStroke** - fret number font weight (default: 0.5)
  * **maxFret** - maximum number of frets - cannot be greater than 15 (default: 15)
  * **show1st** - whether to always show 1st fret number and start the chord image from lowest fretted note (default: false)
  * **zIndex** - CSS z-index should be higher than z-index of the rest of web page, which is usually 0 (default: 99)
  * **zoom** - overall zoom useful to quickly enlarge graphic without messing with individual parameters (default: 1)