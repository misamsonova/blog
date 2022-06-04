---
title: The design of the report in Markdown
subtitle: Hi! 👋 Today I will talk about the design of the report in Markdown. Let's get started!

# Summary for listings and search engines
summary: Hi! 👋 Today I will talk about the design of the report in Markdown. Let's get started!
# Link this post with a project
projects: []

# Date published
date: '2022-05-14T00:00:00Z'

# Date updated
lastmod: '2022-05-14T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin
  - 吳恩達

tags:
  - Academic
  - 开源

categories:
  - Demo
  - 教程
---

This document is intended to familiarize the user with the functionality of the Markdown markup language.
Markdown is a lightweight markup language that is a tool for converting code to HTML.
The main feature of this language is the simplest syntax, which serves to simplify writing and reading markup code, which, in turn, makes it easy to correct it.
Now let's take a closer look at the functions of the Markdown markup language.

Markdown is not a replacement for HTML. The Markdown syntax is quite limited, and corresponds to only a small subset of HTML elements. It includes the following elements:

1. Block elements
+ [Paragraphs and Line Breaks](#Parag);
+ [Headers](#Headers);
+ [Quotes](#Blockquotes);
+ [Lists](#Lists)
+ [Code Blocks](#CodeBlocks);
+ [Horizontal (dividing) lines](#Lines).
2. Lowercase elements
+ [Links](#Links);
+ [Text Selection](#Emphasis);
+ [Code fragments of strings](#Code);
+ [Images](#Images).
3. Additional elements
+ [Backslash](#Backslash Escapes);
+ [Automatic Links](#Automatic Links);
+ [HTML Special Characters](#SpecialSymbol).

For more information about the listed functions, see the section "Syntax Description".

SYNTAX DESCRIPTION
=========================

Block elements
--------------------------

##### <a name="Parag"></a> Paragraphs and line breaks
In order to create a paragraph using the syntax of the Markdown language, it is enough to separate the lines of text with one (or more) empty line (any line that contains nothing but spaces and tab characters is considered empty).
In order to insert a visible line break (the `<br/>` element), you must end the line with two spaces and press the "Enter" key.
Many elements of the Markdown syntax look and work much better when they are formatted using "hard line translation" (line separation performed by the user himself, and not by the program automatically). Such elements include quotes, lists, etc.

##### <a name="Headers"></a> Headings
The Markdown markup language supports 2 styles of heading designations: underlining and highlighting with a symbol ("#").
Headings are highlighted using underscores with equal signs ("=") if the title is of the first level, and hyphens ("-") if the title is of the second level. The number of underscores is not limited.
When selecting headers using the symbol ("#"), from one to six of these characters are used, which are set at the beginning of the line (before the header). In this case, the number of characters corresponds to the header level. In addition, it is possible to provide the title with closing characters ("#"), although this is not mandatory. The number of closing characters does not have to match the number of initial characters. The level of the title is determined by the number of initial characters.
The headings of the first and second levels, made using underscores, look like this:

First level header
========================
Second level header
-------------------------

The headers of the first, third and sixth levels, made using the symbol ("#"), look like this:

# The header of the first level
### Third level header
###### Sixth level header
The above headings made with the symbol ("#") are identical to the following:

# First level header #
### Third level header ###
###### Sixth level header ######
As a result, the following is displayed on the screen:

First level header
========================

Second level header
------------------------

# First level header
### Third level header
###### Sixth level header

##### <a name="Blockquotes"></a> Quotes
The Markdown language uses the "more" (">") sign to indicate quotations. It can be inserted both before each line of the quotation, and only before the first line of the paragraph.
Also, the Markdown syntax allows you to create nested quotes (quotes inside quotes). Additional levels of citation marks (">") are used to mark them.
Quotes in Markdown can contain all kinds of markup elements.
Quotes in the Markdown language look like this:

>This is an example quote,
>in which
an angle bracket is placed before each line >.

>This is an example quote,
in which the angle bracket
it is put only before the beginning of a new paragraph.
>The second paragraph.

Embedding a quote into a quote looks like this:

> First Citation level
>> Second level of citation
>>> Third level of citation
>
>First Citation level
As a result, the following is displayed on the screen:

>This is an example quote,
>in which before each line
>an angle bracket is placed.

>This is an example of a quote
in which an angle bracket
is placed just before the beginning of a new paragraph.

>The second paragraph.

Enclosed quote:

> First Citation level
>> Second level of citation
>>> Third Citation Level
>
>First Citation Level


The citation level cannot exceed the 15th.

##### <a name="Lists"></a> Lists
Markdown supports ordered (numbered) and unordered (unnumbered) lists.
Markers such as asterisks, pluses, and hyphens are used to form unordered lists. All the listed markers can be used interchangeably.
To form ordered lists, numbers with a dot are used as markers. An important feature in this case is that the numbers themselves, with which the list is formed, are not important, since they do not affect the output HTML code. No matter how the user numbers the list, the output will in any case have an ordered list starting with one (1, 2, 3 ...). This feature should be taken into account when it is necessary to use the ordinal numbers of the elements in the list so that they correspond to the numbers obtained in HTML.
Ordered lists should always start with one. List markers usually start from the beginning of the line, however, they can be shifted, but not more than 3 spaces. The marker must be followed by a space or a tab character.
If necessary, you can insert a quote into the list. In this case, the citation notation (">" ) should be indented.
The ordered lists look like this:

1. Explorer
2. Semiconductor
3. Dielectric

The unordered lists look like this:

* Explorer
* Semiconductor
* Dielectric

Or

- Guide
- Semiconductor
- Dielectric

Or

+ Explorer
+ Semiconductor
+ Dielectric
The output of all three listed options has the same result.
As a result, the following is displayed on the screen:

1. Explorer
2. Semiconductor
3. Dielectric

and

+ Explorer
+ Semiconductor
+ Dielectric

The quote inserted into the list looks like this:

1. A list item with a quote:

> This is a quote
> inside the list item.

2. The second item of the list

As a result, the following is displayed on the screen:

1. A list item with a quote:

> This is a quote
> inside the list item.

2. The second item of the list


When inserting quotes into the list items, it is important to keep in mind that the list items must be on the same level, and quotes must be indented. If the rule with a single list level is not followed, the next item in the list after the quote will be automatically numbered with the digit "1."
In addition, if necessary, you can insert the source code into the list. In this case, it should be written with double indentation – 8 spaces or 2 tab characters.

- A list item containing the source code

<source code >

##### <a name="CodeBlocks"></a> Code blocks
Formatted code blocks are used when it is necessary to quote the source code of programs or markup.
To create a block of code in the Markdown language, it is necessary to start each line of a paragraph with an indent consisting of four spaces or one tab character. The code block continues until there is a line without indentation (or the end of the text). Inside the code block, ampersands ("&") and angle brackets ("<" and ">") are automatically converted into HTML markup elements. In addition, it should be noted that inside the code blocks, the usual Markdown syntax is not processed.
The code block in Markdown looks like this:

This is a regular paragraph:

This is a block of code

##### <a name="Lines"> </a> Horizontal lines (separators)

In order to create a horizontal line using the Markdown syntax, you need to place three (or more)a hyphen or asterisk on a separate line of text. It is possible to place spaces between them.
Horizontal lines in Markdown look like this:

The first part of the text to be divided
***
The second part of the text that needs to be divided

Or

The first part of the text to be divided

---

The second part of the text that needs to be divided
As a result, the following is displayed on the screen:

The first part of the text to be divided
***
The second part of the text that needs to be divided

When using this tool, it is important to remember that an empty line must be left after the first part of the text and before the second. This rule must be observed only when using hyphens. If it is not followed, the second-level header and a line of plain text will be displayed on the screen. When using the asterisk symbol, this rule can be ignored.

Lowercase elements
-------------------

##### <a name="Links"></a> Links
Markdown supports two styles of link design:

- Hyperlink, with immediate indication of the address (in-text);
- A hyperlink similar to a footnote.

It is assumed that in addition to the URL, there is also a link text. It is enclosed in square brackets.


