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

[3] Unicode Properties in Character Proposals
http://unicode.org/pending/properties.html <br>

a more-or-less complete list of properties
http://www.unicode.org/reports/tr44/#Properties

[4] JavaScript has a Unicode problem
https://mathiasbynens.be/notes/javascript-unicode <br>

[5] JavaScript’s internal character encoding: UCS-2 or UTF-16?
https://mathiasbynens.be/notes/javascript-encoding#surrogate-formulae <br>
_BMP(Basic Multilingual Plane):_  U+0000 to U+FFFF

> Characters outside the BMP, e.g. U+1D306 tetragram for centre (𝌆), can only be encoded in UTF-16 using two 16-bit code units: 0xD834 0xDF06. This is called a surrogate pair. Note that a surrogate pair only represents a single character.

> The first code unit of a surrogate pair is always in the range from **0xD800 to 0xDBFF**, and is called a high surrogate or a **lead surrogate**.

> The second code unit of a surrogate pair is always in the range from **0xDC00 to 0xDFFF**, and is called a low surrogate or a **trail surrogate**.

> Converting between code points and surrogate pairs
https://mathiasbynens.be/notes/javascript-encoding#surrogate-formulae
```
H = Math.floor((C - 0x10000) / 0x400) + 0xD800
L = (C - 0x10000) % 0x400 + 0xDC00

reverse mapping
C = (H - 0xD800) * 0x400 + L - 0xDC00 + 0x10000
```
https://www.ecma-international.org/ecma-262/8.0/index.html#sec-utf16encoding
<br>

ECMAScript Conformance
https://www.ecma-international.org/ecma-262/8.0/index.html#sec-conformance <br>

ECMAScript Source Text
https://www.ecma-international.org/ecma-262/8.0/index.html#sec-source-text <br>

> ECMAScript code is expressed using Unicode. ECMAScript source text is a sequence of code points. All Unicode code point values from **U+0000 to U+10FFFF**, including surrogate code points, may occur in source text where permitted by the ECMAScript grammars. The actual encodings used to store and interchange ECMAScript source text is not relevant to this specification. Regardless of the external source text encoding, a conforming ECMAScript implementation processes the source text as if it was an equivalent sequence of **SourceCharacter** values, each SourceCharacter being a Unicode code point.

> Surrogate pairs are only recombined into a single Unicode character when they’re displayed by the browser (during layout). This happens **outside of the JavaScript engine**.
<br>

[6] JavaScript character escape sequences
https://mathiasbynens.be/notes/javascript-escapes

- Single character escape sequences

- Octal escape sequences
> A conforming implementation, when processing strict mode code, **must not** extend the syntax of EscapeSequence to include `LegacyOctalEscapeSequence` as described in B.1.2.

> It’s probably easiest to define octal escape syntax using the following regular expression: `\\(?:[1-7][0-7]{0,2}|[0-7]{2,3})`.

- Hexadecimal escape sequences
> You could define hexadecimal escape syntax using the following regular expression: `\\x[a-fA-F0-9]{2}`.

- Unicode escape sequences
> Any character with a character code **lower than 65536** can be escaped using the hexadecimal value of its character code, prefixed with `\u`.

> Unicode escapes are **six** characters long. They require exactly four characters following `\u`.

> You could define Unicode escape syntax using the following regular expression: `\\u[a-fA-F0-9]{4}`.

- ECMAScript 6: Unicode code point escapes
> When this is implemented, **any character** can be escaped using the hexadecimal value of its character code, prefixed with `\u{` and suffixed with `}`. This is allowed for code points up to `0x10FFFF`, which is the highest code point defined by Unicode.

> You could define Unicode code point escape syntax using the following regular expression: `\\u\{([0-9a-fA-F]{1,})\}`.

- Control escape sequences
> In **regular expressions** (not in strings!), any character with a character code greater than `0` and lower than `26` can be escaped using its caret notation character, prefixed with `\c`.

> Control escapes are **three** characters long. They require exactly one character following `\c`.

> You could define control escape syntax using the following regular expression: `\\c[a-zA-Z]`.
<br>

JS escape tool:
https://mothereff.in/js-escapes





