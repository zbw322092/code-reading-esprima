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
<br>

[3] Line Terminators
https://www.ecma-international.org/ecma-262/8.0/index.html#sec-line-terminators

> A line terminator cannot occur within any token except a `StringLiteral`, `Template`, or `TemplateSubstitutionTail`.

> A line terminator can occur within a `MultiLineComment` but cannot occur within a `SingleLineComment`.

> Line Terminator Code Points
https://www.ecma-international.org/ecma-262/8.0/index.html#table-33

``` javascript
  isLineTerminator(cp: number): boolean {
    return (cp === 0x0A) || (cp === 0x0D) || (cp === 0x2028) || (cp === 0x2029);
  }
```
<br>

[4] What is the difference between a “line feed” and a “carriage return”?
https://stackoverflow.com/a/12747850

> A line feed means moving one line forward. The code is \n.
A carriage return means moving the cursor to the beginning of the line. The code is \r.
Windows editors often still use the combination of both as \r\n in text files. Unix uses mostly only the \n.
<br>

[5] Comments
https://www.ecma-international.org/ecma-262/8.0/index.html#sec-comments

> Comments can be either single or multi-line. Multi-line comments cannot nest.
<br>

[5.1] three kinds of javascript comments
http://www.javascripter.net/faq/comments.htm
<br>


[6] White Space
> White space code points may occur within a `StringLiteral`, a `RegularExpressionLiteral`, a `Template`, or a `TemplateSubstitutionTail` where they are considered significant code points forming part of a literal value. They may also occur within a `Comment`, but cannot appear within any other kind of token.

> White Space Code Points
https://www.ecma-international.org/ecma-262/8.0/index.html#table-32
<br>

[7] Reserved Words
https://www.ecma-international.org/ecma-262/8.0/index.html#sec-reserved-words

? Esprima implementation about `reserved words` seems different from ECMAScript Stanard(link above).
<br>

[8] String Literals
https://www.ecma-international.org/ecma-262/8.0/index.html#sec-literals-string-literals


















