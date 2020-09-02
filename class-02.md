# Reading Notes Class 02

## Structural markup
- elements used to describe both headings and paragraphs
## Semantic markup
- extra info
    - emphasis placed in a sentence
    - quotation
    - meaning of an acronym 
## headings 
- <h1>
- etc
## paragraphs
- <p>
## bold
- <b>
## italic
- <i
## superscript
- <sup>
## subscript
- <sub>
## white space
- white space collapsing when it all comes together 
#3 line breaks and horizontal rules
- <br /
- <hr /
- empty elements are written differently
## visual editors and their code views
- visual and code view differenciation 
## semantic markup
- do not affect the structure
- add extra info to the pages
    - <em emphasis
    - <strong strong importance
    - <blockquote longer quotes that take a paragraph
    - <q for shorter quotes
    - <abbr abbreviations
    - <cite citations
    - <dfn definitions
    - <address contact details for the author of the page
    - <ins content inserted
    - <del content has a line through it
    - <s indicates something that is no longer accurate or relevant... but that should not be deleted

# CSS
## CSS selectors
- universal 
    - *{} targets all elements on the page... universal
- type selector
    - h1, h2, h3 {} targets the <h1> etc elements
- class selector
    - *note {} targets any elemnt whose class attribute has a value of note
    - p.not {} targets only <p> elements whose attribute has a note
- id selector
    - #introduction {} targets id attributes ahd value of introduction 
- child selector
    - li>a {} any <a> elements that are children of an <li>
-descendant selector
    - p a {} 
- adjacent sibling selector
    -hl~p {} targets first <p> after any <h1>
- general sibling selector
    - hl~p {} rule to apply to sibling elements

## External CSS
- <link
- href
- type
- rel
## internal CSS
- <style
## CSS rules cascade
## font inherited, background color & border properties are not

# all major browsers use a JS interpreter to translate your js instructions into something the computer can follow
1. browser receives HTML page
2. creates a model of the page and stores it to memory
3. show the page on screen using a rendering engine


## creating a basic javascript
- written in plain text just as html and css
- see example from 102 (pg 47)

## statements
- if
- else if

## comments
- //

## variable
- place data is stored for bits of info toward a function
- data change change in a var
- can store a boolean

## data types
- numerical
- string
- true

## use true and false to change value of var
## rules for naming variables
1. name must begin with a s $ or and _ and must not start with a number
2. can contain letters, dollar sign or and underscore
    -must not use a dash or period
3. cannot use keywords or reserved words
4. case sensitive
5. name describes the kind of info var stores
6. Capital letter for every word after the first if more than one word

## arrays
- stores a list of values
- separated by commas

## expressions
- expression results in a single value
    1. exp that assign a value such as color
    2. esp that use two or more values to return a single value such as addition 3*2 
## operators
- assignment such as a 
    - color value
    - basic math
    - combine two strings 'hi ' + 'Gus'
- comparison operators
    - compare two to return a true or false buy = 3 > 5
    - combine to return a true or false buy = (5 > 3) && ( 2 < 4> )
### math operators
- + add
- - subtract
- / divides
- (*) multiplies
-  ++ increment
- -- decrement
- % divides two with a remainder

## string operator
- joining two or more strings for one concatenation 
- use quotes around a numerical value 

## evaluations -analyze values
## decisions -decisions
## loops -loops
 -  == equal to
 - != not equal
 - === compares two values
 - !== strict not equal to
 - > greater than
 - < less than 
 - <= less than equal to
 - >= greater than equal to
 ## local operators
 - && logical and 
 - || logical or 
 - ! logical not 

 ## key concepts
 - break termination of a loop 
 - continue stop the current iteration and check again
 ## for loops
 - to loop through items in an array
    - arrayLength total items in an array stored in a var 
    - roundNumber three or more var
    - innerHTML msg var is written into the page
 ## while loops
 ## do while loops
 - statement comes before  the condition





From the Duckett HTML book:

Chapter 2: “Text” (pp.40-61)
Chapter 10: Ch.10 “Introducing CSS” (pp.226-245)
From the Duckett JS book:

Chapter 2: “Basic JavaScript Instructions” (pp.53-84)
Chapter 4: “Decisions and Loops” only up to the section on switch statements (pp.145-162)