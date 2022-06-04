---
title: Easy markup languages
subtitle: Hi! 👋 Today I will talk about lightweight markup languages. Let's get started!

# Summary for listings and search engines
summary: Hi! 👋 Today I will talk about lightweight markup languages. Let's get started!
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

# What is a "markup language"?
**Markup language** is a set of codes that, when applied to plain text, allows you to add one or more of the following properties (among others):
- Define the text
- Structure the text
- Describe the layout of the text
- Decorate the text
One markup language you encounter every day (unless you're a hermit) is hypertext markup language, or HTML. Websites and apps that bring you news and show you your email are built, at least in part, with HTML markup using tags as a mechanism to mark up raw text content. For example, consider the following HTML fragment:
<body> <h1>Introducing HTML</h1> <p>Here is a paragraph in HTML... we know it's a <strong>paragraph</strong> because the surrounding \<p\> tags define it as one.</p> </body>

Here, the "p" tag indicates that all subsequent text, up to the closing </p> tag, is a paragraph. In this sense, it defines the text as a paragraph.

But pay attention also to the "body" tags... they often serve to determine the layout of a web page, for example, how many fields are on the side of the screen.

And the "strong" tags will decorate the word "paragraph" in bold, and the "h1" tags can both mark up the title (separate it from the surrounding text) and define a larger font.

The problem with some markup languages (among them HTML) is that entering these tags manually is a very tedious task. And with other languages like XML, tags and their attributes make up more of the overall content than the text itself!

# Enter a lightweight markup language
If you wanted to take advantage of markup languages, for example by publishing an HTML page on the internet or converting a DocBook file to PDF so that it could be printed, you had to do one of two things. On the one hand, you can spend time learning these languages inside and out, writing them down manually, and then checking your work three times. Or you could invest the money in a tool that manages the complexity of them for you.

Fortunately, some enterprising developers have come up with a third option. They created new markup languages that contained many (in some cases most or all) of the functions of heavier analogues, but greatly simplified the syntax. These "light" languages include the familiar Markdown as well as Asciidoc, the Egc format in Org mode and the Mediawiki syntax.

# Lightweight markup languages have a simple syntax

One of the distinguishing features of these languages is that their "tags" (such as they are) should be intuitive. Let's look at the previous fragment, this time written in Asciidoc:

"Introducing Asciidoc -------------------- Where are the *paragraph* tags? We dont need them... Asciidoc is smart enough to realize this is a paragraph!"

Much more readable, no? Starting from the top, we can identify the title, since it is "underlined" with strokes. You could do this if you were writing by hand, just draw an underscore under the page title in notepad. There are also no paragraph tags — Asciidoc treats anything between two empty lines that don't have any other markup on them as "plain" paragraph text. Finally, the asterisks around the word "paragraph" are indicated in bold. Raise your hand if you did it in a text message to mean the same thing.

Each has one or more corresponding processors
Heavy-weight markup languages usually have a special application for their interpretation. On the Internet, your browser and, possibly, a web server will turn the code into bright web pages. For documents in XML format, it can be something like Microsoft Word, which reads and writes in DOCX format. (this is another XML dialect). This way you will never have to interact directly with the source of these documents, only the cute facades that your applications show.

Meanwhile, documents written in light languages are read by a person in their original form (another tenant), but only true nerds can consider them beautiful. To get a good result, you need to use a processor. These are applications that will consistently go through your markup and transform it into something else that looks good. The same projects that develop the language itself, as a rule, create a utility for its use. The Markdown project offers a Perl script with the same name, and the accompanying Asciidoc program is written in Python. In addition, other conversion utilities will include support for some of these languages. One such example is the excellent Pandoc, which will use Markdown, as well as lightweight tagging, restructured text, Mediawiki and Org-Mode and convert them to PDF, DOCX, ODT and others.

# Asciidoc markdown Pandoc formats

As a result, lightweight markup languages allow you to work with plain text, the most portable data format on the planet, but in the end they still give a beautiful result. Now that you are convinced of its merits, which language to choose? Markdown is undoubtedly the most popular and has its advantages (more on this later). But Asciidoc, in particular, is a worthy alternative. In the next section, we'll look at a few reasons why.

# Comparison of Markdown and Asciidoc

The Asciidoc format was created to simplify DocBook, one of the most common formats when writing long (especially technical) texts. One of the requirements for fame is that it is a one-on-one translation, that is, for each element in the DocBook there is a corresponding representation in Asciidoc. Below we will look at some pros and cons of Asciidoc compared to Markdown.

# Asciidoc covers a superset of written elements

The goal of Markdown from the very beginning was to create a simple format for web writers. Thus, the entry elements it supports (at least the original implementation, see below) are aimed at automating the more time-consuming aspects of HTML writing (lists, for example, that require <ol> or <ul> tags in addition to <li> tags for each element).

# Complex asciidoc markdown formats

Asciidoc also contains them, but also offers more advanced DocBook elements, such as warnings (for example, "Note:" or "Info:" callout blocks) and complex table layouts. That doesn't mean you have to use them all the time, but they will be there and available if you ever need them.

# Asciidoc is a single format

When the popularity of Markdown began to decline, some of its users began to face some of the disadvantages described above. So these users started developing their own extensions to solve these problems, such as the ability to add tables or footnotes/notes. Soon, many "flavors" of Markdown appeared, including (among others):

The flavor used by Github for the "Readme" files of the projects it hosted.
An "extended" version based on the PHP port of the original Markdown, with additional HTML-related features.
A fragrance called "MultiMarkdown", which implements many functions of writing longer forms, including citations, definitions and cross-references.
As a result, your document may require elements that are not all covered by the same flavor. In contrast, Asciidoc does not suffer from the same fragmentation as Markdown currently does.

# Asciidoc is aimed at a variety of publishing styles

Markdown is great for quickly getting a blog post out of your head and onto the page. But out of the box it is not designed to structure longer works like a book. Asciidoc is designed for this, and one example is its "enable" functions. These operators allow you to include the entire contents of one file in another:
include::somefile.adoc

This is not much different from how basic documents work in text editors. This allows, for example, to compose each chapter as a separate file, and then "include" them all in one file representing the book. When you process this "book file", the result will be as if all the chapters were written directly into this document.

#Markdown is enough for most users

Markdown covers all the basics for most users. For those who are just looking for a blog or printing some notes in text format, Markdown supports all the elements they will need. Cross-references mean little to a user who just wants to create a simple note or web page. You could even use Markdown for longer works with simple layouts like roman" and combine them yourself at the end.
