## What CSS does
- block and inline elements
- style rules with html elements
- css properties affect how elements are displayed 
- link css to use externally

## Selectors
- universal selector applies to all elements in doc      * {}
- type selector matches element names       h1,h2,h3 {}
- class selector matches element whose class attribute has a value that matches the one specified after the period symbol       .note {}    p.note {}
- id selector matches an element wose id attribute has a vlaue that matches the one specified after the hash symbol     #introduction {}
- child selector mathces an element that is a direct child of another       li>a {}
- decdendant selector matches and element that is a descendebt of another specified element (not just a direct child of the element)        p a {}
- adjacent sibling selector matches and element that is the next sibling        h1+p {}
- genereal sibling selector matches and element that is a sibling of anther (doen't to be the direct preceding element)     h1~p {}

## CSS rules cascade
- if two selectors are the same the latter of the two will take precedence
-if one is more specific than the others - the mroe specific will take presedence 

## inheritance
- if you specify font family or color proberties on the <body> they will apply to most child elements
- example: background color or boarder properites are not inherited 