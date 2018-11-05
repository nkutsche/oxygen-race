# Nico's Oxygen Navigation Race 

For developers of large and very complex programs a basic challange is to keep the overview of there code. Finding of usage of variables, navigating to function declarations, searching for specific code lines – all these are usual and basic tasks of navigation in code projects.

Fast and eficient navigation is very important for the developers. Beside of saving time, they are able to focus on the essential: the logic of the code. If you search to long for the correct code line, you will forget, why you searched for it.  

Modern and powerfull IDEs provides many functions to help the developers on the complex navigation.
Basically each has an search and replace function, but by analyzing the code, it is able to lead the developers much more precise to their search result.
For instance it knows by compiling the code where functions or variables was declared and can respect language specific rules like function overloading or variable scopes.  

In the XML world one of the leading IDEs is the Oxygen XML Editor and it is also my favorite. One reason is, that it has lots of little features, hints and tricks for better navigation in and editing of XSLT stylesheets. I have now 10 years experiences with Oxygen, but I'm still not sure, that I found everything.

But how can you find these tricks? Some of them are really not very easy to find. Looking back, I have to say: I have found some features by browsing the Oxygen preferences, some by getting a hint from other developers, but most of it, I found by mistyping or miss-clicking.

In other words: ***Who reads the fucking manual, anyway?***

Even if I would read the Oxygen manual completely, I would forget the most of it, if I don't use it immediately. 

To teach our new developers of data2type in Oxygen, I wanted to make it more interesting. Also I wanted to demonstrate, how fast you can be if you know the tricks. So I had the idea of the *Oxygen Navigation Race*. The Oxygen Race is a game similar to a treasure hunt or scavenger hunt ("Schnitzeljagd"). The race participants has to follow instructions in the correct order. The instructions are spread throughout a large XSLT stylesheet. Each instruction leads to the next instruction. The participants are free to use any tool of Oxygen (with one obvious exception) to find the next goal.

The Oxygen Race makes fun, but each step is also a demonstration of at least one Oxygen feature.

## Start and Rules

To start, just open the 
[Oxygen project](oxygen-race.xpr) in the Oxygen and open there the 
[start.xhtml](oxygen-race-en/start.xhtml). But don't forget to check the 
[rules](oxygen-race-en/rules.xhtml) before you start.

## Solution

In the "solution" folder, I describe, how I would make the race, as:

- [Description](solution/Solution.md)
- [Video](solution/solution.gif)

Please let me know if you know for a step a shorter way or know a feature, which is not covered by the current race.

## Oxygen Editing Challenge

The next similar project would be the Oxygen Editing Challenge. The Navigation Race is focused on jumping from one code line to another. What I'm still missing is, the lots of Oxygen features, which helps the developer to *edit* an XSLT stylesheet. I see much potential, but I'm not sure how to implement it. I'm open for suggestions. 