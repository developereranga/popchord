# Exceptions #

In case of error popchord will throw javascript **_Error_** that can be caught by **_onerror_** event handler in the following way:
```
window.onerror = function (msg, url, line) 
{
 // do something with parameters like:
 alert("Caught: '" + msg + "' from " + url + ":" + line);
}
```
where:
  * msg - error description string passed by popchord
  * url - full url of script file (in this case popchord.js)
  * line - line number from file from above that generated this exception

Please note that exceptions can only pass string type argument with error description. The browsers may append or prepend this string by additional substrings (like **_Error:_** or similar), so if you want to do something with these messages you'll need to parse them using regular expression functions.

There are two type of exeptions:

### 1. Fatal Errors ###
Fatal error terminates **_chordInit()_** call so none of the chords will be initialized. Your page will look like normal plain text with chord names but without any chord graphics. They are generated in parameter validation section and therefore are prefixed with **_Validate:_**. There are currently 2 validate errors with messages that are self-explanatory:
```
'Validate: parameter [numString=(number of strings)] must be > 1'

'Validate: parameter [nameClass=(class name)] may only contain letters a-z. A-Z, -, _ and numbers 0-9'
```

### 2. Non-fatal Errors ###
Non-fatal error terminates chord rendering procedure initiated by **_mouseover_** event, so it affects only invalid chords, while all remaining chords will be normally displayed on the page. These are prefixed with **_Chord:_**. At present there are 2 chord errors:
```
'Chord: [(chord name)] description [(chord definition string)] must have exactly (number of strings) characters')

'Chord: [(chord name)] description [(chord definition string)] may only contain numbers 0-9 and letters a-f, A-F, x and X'
```