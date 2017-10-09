## ECMAScript Lexical-Grammar
[1]
> The source text of an ECMAScript Script or Module is first converted into a sequence of input elements, which are tokens, line terminators, comments, or white space. The source text is scanned from left to right, repeatedly taking the longest possible sequence of code points as the next input element.
<br>

[2]
ECMAScript `IdentifierName`:
> `IdentifierName` but not `ReservedWord`
https://www.ecma-international.org/ecma-262/8.0/index.html#prod-Identifier

- Unicode Property Table
http://www.unicode.org/reports/tr44/#Property_List_Table <br>

- Unicode `ID_Start` and `ID_Continue`
http://www.unicode.org/reports/tr41/tr41-21.html#UAX44 <br>

- UNICODE IDENTIFIER AND PATTERN SYNTAX
http://www.unicode.org/reports/tr31/tr31-27.html
  > Conformance
  The following describes the possible ways that an implementation can claim conformance to this specification.
  http://www.unicode.org/reports/tr31/tr31-27.html#Conformance

  > Default Identifier Syntax
  http://www.unicode.org/reports/tr31/tr31-27.html#D1
  `<Identifier> := <Start> <Continue>* (<Medial> <Continue>+)*`
  <br>

  > Properties for Lexical Classes for Identifiers
  http://www.unicode.org/reports/tr31/tr31-27.html#Table_Lexical_Classes_for_Identifiers

- `<ZWNJ>` and `<ZWJ>`
  https://en.wikipedia.org/wiki/Zero-width_joiner
  https://en.wikipedia.org/wiki/Zero-width_non-joiner
  http://www.unicode.org/L2/L2002/02363-nelson-zwj-zwnj.pdf

  > ZERO WIDTH NON-JOINER (ZWNJ – U+200C) and ZERO WIDTH JOINER (ZWJ –
  U+200D) to control the **formation of ligatures**.











