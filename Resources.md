## Unicode
[1] what is Unicode
http://unicode.org/standard/WhatIsUnicode.html <br>

[2] Unicode® 10.0.0
http://www.unicode.org/versions/Unicode10.0.0/ <br>

[3] About the Unicode® Standard
http://www.unicode.org/standard/standard.html <br>

[4] Unicode 10.0 Character Code Charts
http://www.unicode.org/charts/ <br>

[5] Unicode and ISO 10646
http://unicode.org/faq/unicode_iso.html
> So are they the same thing?

> No. Although the character codes and encoding forms are synchronized between Unicode and ISO/IEC 10646, the Unicode Standard imposes additional constraints on implementations to ensure that they treat characters uniformly across platforms and applications. To this end, it supplies an extensive set of functional character specifications, character data, algorithms and substantial background material that is not in ISO/IEC 10646.
<br>

[6] The Unicode® Standard: A Technical Introduction
http://www.unicode.org/standard/principles.html
> The Unicode Standard is the universal character encoding standard used for representation of text for computer processing.

> The design of Unicode is based on the simplicity and consistency of ASCII, but goes far beyond ASCII's limited ability to encode only the Latin alphabet. The Unicode Standard provides the capacity to encode all of the characters used for the written languages of the world.

> The Unicode Standard and ISO/IEC 10646 support three encoding forms (UTF-8, UTF-16, UTF-32) that use a common repertoire of characters. 
<br>

[7] UTF-8, UTF-16, UTF-32 & BOM
http://www.unicode.org/faq/utf_bom.html
<br>

[8] Code point
https://en.wikipedia.org/wiki/Code_point

> In character encoding terminology, a code point or code position is any of the numerical values that make up the code space.[1] Many code points represent single characters but they can also have other meanings, such as for formatting.

> Unicode comprises 1,114,112 code points in the range 0hex to 10FFFFhex. The Unicode code space is divided into seventeen planes (the basic multilingual plane, and 16 supplementary planes), each with 65,536 (= 216) code points. Thus the total size of the Unicode code space is 17 × 65,536 = 1,114,112.
<br>

[9] Unicode Codepoint Chart
http://inamidst.com/stuff/unidata/ 
<br>

## ECMAScript Encoding
[1] ECMAScript Language: Source Code
https://www.ecma-international.org/ecma-262/8.0/index.html#sec-ecmascript-language-source-code
> SourceCharacter::
any Unicode code point

> ECMAScript code is expressed using Unicode. ECMAScript source text is a sequence of code points. All Unicode code point values from U+0000 to U+10FFFF, including surrogate code points, may occur in source text where permitted by the ECMAScript grammars

*[2] UTF-16
https://en.wikipedia.org/wiki/UTF-16 <br>
