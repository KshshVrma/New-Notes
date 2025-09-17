[[SQL Joins]]

base64:
<img src="https://www.researchgate.net/publication/275415203/figure/fig4/AS:398565261234176@1472036771078/Base64-Encode-Conversion-Algorithm.png"/>

the output is 33% larger
used to encode binary data so that it can be sent via mails,etc
converts very  3 -> 8 bit chars to 4 -> 6 bit chars


Unicode:
and specially utf encoding solves the problem of encoding the other languages which are not supported by ascii test

the benefits are that for the lower value  , 65 maps to A in both ascii and utf, that is why it is backward compatible with asciiii

similar to ascii there is mapping of letters to numbers, 

utf-32:

maps each character to 4 bytes, 
this gives equal representation to other languages but, it wastes a lot of space because most of the thing in the webpages are in english because of html being the markup languae so inroder to reduce the space, for frequentyly used characters we use utf-8

utf-8:
this is a variable mapping , so by that it means that it maps some character eg which are english and frequently used as a single bytle, and other chars for eg a emoji with upwards of 4 bytes, so it maps from 1-4 bytes.


so the change goes like this:
encoding->
char-> mapped to number based on encoding -> binary form of the number
<-decoding
