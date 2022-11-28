# Nico's Oxygen Navigation Race – Solution

There is no general solution for the Oxygen Race. The following "solution" describes only, how I would do it. You may have alternative tricks, which are faster or at least faster for you.

## Step by step

Let's go Step-by-Step:

### STEP 1: Go at the beginning of the following document

Press `ctrl` and click on the value of the `href` attribute (`href="oxygen-race.xslt#start"`). You will imidiately jump to the start of the document. This works, because Oxygen detects `href` attributes and knows that this path points to a document. The suffix `#start` points to any ID. In document formats with no specific ID you can define `xml:id="start"` attributes.

### STEP 2: Go at the end of this documents!

Press `ctrl`+`end`.
This is a basic feature of many editors. 

### STEP 3: Where was this parameter was used?

On the right side next to the vertical scroll bar you'll find a, let's call it, *marker bar*. On this bar you will find markers for errors, but also interactivly for items you are selecting and which are referend somewhere else.

So, click on the name of the parameter (`name="variable"`). And you will see the marker where this parameter was used. By clicking on the marker you will jump directly to it. 

### STEP 4: Where was this parameter declared?

Press `ctrl` and click on the paremter (`$parameter2`). You will jump to the declaration of this parameter. You may notice that this parameter was declared in a separate stylesheet *oxygen-race-include.xslt*. This was included by the main stylesheet. Oxygen recognize this and opens the stylesheet to find the declaration.

### STEP 5: Where was this template declared?

Press `ctrl` and click on the name of the called template (`"template"`). You will jump to the declaration of this template.

In opposite to the step before, Oxygen can not know automatically, where this template was declared, because there is no reference from the included stylesheet to the main stylesheet. This works only, because there was a basic setup in the Oxygen project *oxygen-race.xpr*. You can select any project resource folder and let Oxygen detect the "Master files". Master files should be the stylesheets which are including any other involved stylesheets and should not be included somewhere else. 

The Master files are stored in the project, so Oxygen remembers the includes of these files and can resolve references between the files, like this template call.

### STEP 6: Go at the beginning of this template

Click three times at the end tag of the template (`</xsl:template>`) and press the arrow `LEFT`.

### STEP 7: Find all templates which are matching in the mode "fix"

This step is very tricky if you don't know the marker bar (mentioned on STEP 3) and are not so familiar with modes.

That's why there is an alternative way to find STEP 8.

But to finde the STEP 8 directly, you just have to click on the mode name (`"fix"`) and click on the markers in the marker bar. There are two templates which are matching:

One matches to the mode `fix`. This represents the STEP 7a.
The other one matches to the all modes with the key word `#all`. Oxygen respects the templates with this special mode, when you click on a specific mode. Here you'll find the STEP 8.

#### STEP 7a: Find the variable with exact the same content:

This is a searching task. To select the content of the variable easly, you can click three times at the end of the start tag of the variable (`<xsl:variable name="buildIn">`). Oxygen selects the complete content the element. Then press `F3`, the command to search the next occurence of the the selected text.

#### STEP 7b: Find the declaration of the refered format

Press `ctrl` and click on the value of the `format` attribute (`"sqf:fixes"`). You will jump to the declaration of the format.

#### STEP 7c: Where was this format used?

Click on the name of the xsl:output (`name="sqf:fix"`) and you will see the marker on the *marker bar* where this format was used. By clicking on the marker you will jump directly to it.

#### STEP 7d: Where was this template declared?

Press `ctrl` and click on the name of the called template (`"sqf:keep"`). You will jump to the declaration of this template.

### STEP 8: Find the next xsl:message element

Select the start tag of the `xsl:message` element and press `F3`, the command to search the next occurence of the the selected text.

### STEP 9: Go at the beginning of the surrounding template

At the top of the editor, directly below the document tabs, you can find a bar which contains a list of buttons. Each button represents an element, which is an ancestor of the current context (at the cursor position). If you click on the `xsl:template` button, Oxygen selects the complete surrounding template. By pressing the arrow `LEFT` you will jump to the beginning of the surrounding template.  

### STEP 10: Where was this `d2t:function` function declared?

Press `ctrl` and click on the function call (`sqf:function(.)`). You will jump to the declaration of the function.

### STEP 11: Where was this key defined?

Press `ctrl` and click on the string, representing the key name (`'key'`). You will jump to the declaration of the key.

Special feature: The `$key-name` paremter of the `key` function is not an usual reference to the used key, because the key function expects a string value for the key name. This means, that the key name can also be defined by another XPath expression. It is just common practice to specify a static string for the `$key-name` parameter. The Oxygen has implemented an exception to recognize such key references. This works only if the `$key-name` parameter is a static string. 

### STEP 12: Where was this key used?

Click on the name of the `xsl:key` (`name="param"`) and you will see the marker on the *marker bar* where this key was used. By clicking on the marker you will jump directly to it.

Same as for STEP 11: This works only if the `$key-name` parameter is a static string.

### STEP 13: Go to line 612

Press `ctrl` + `L` and Enter 612 in the line field. The Oxygen will jump to the requested line.

### STEP 14: Go back to step 12!

In the tool bar of the Oxygen you will find a button with an arrow in left direction. The name of the button is "back". You can use it to find the last cursor positions.

This button is for shorter go-backs very helpful, but please note, that this button is sometimes a bit buggy. I made the experience, that it was to sensitive and I had to click it too often, but also that I jumped somewhere, where I didn't expected it. 

### STEP 15: Open this document

Click at the document path (`'oxygen-race-finish.xml'`) and press `ctrl` + `ENTER`.

## Solution video

If the step-by-step description was not sufficient or confusing to you, I made a screen recording video of one of my race:

![solution.gif](solution.gif)


